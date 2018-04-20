<style>
table {
  border-collapse: collapse;
  border-spacing: 0;
}
</style>

<template>
    <div>

        <Table border :columns="columns2" height="240" :data="data4"></Table>

    </div>
</template>
<style lang="less">
html,
body,
body > div,body > div>div {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}
nav {
  display: none;
}
</style>

<script>
export default {
  data() {
    return {
      isCollapsed: false,
      columns1: [
        {
          title: "Name",
          key: "name",
          align: "center",
          minWidth: 100,
          maxWidth: 200,
          fixed: "left",
          filters: [
            {
              label: "Joe",
              value: 1
            },
            {
              label: "John",
              value: 2
            }
          ],
          filterMultiple: false,
          filterMethod(value, row) {
            if (value === 1) {
              return row.name === "Joe";
            } else if (value === 2) {
              return row.name === "John Brown";
            }
          }
        },
        {
          title: "Other",
          align: "center",
          fixed: "left",
          children: [
            {
              title: "Age",
              key: "age",
              align: "center",
              minWidth: 100,
              maxWidth: 200,
              sortable: true
            },
            {
              title: "Address",
              align: "center",
              children: [
                {
                  title: "Street",
                  key: "street",
                  align: "center",
                  minWidth: 100,
                  maxWidth: 200
                },
                {
                  title: "Block",
                  align: "center",
                  children: [
                    {
                      title: "Building",
                      key: "building",
                      align: "center",
                      minWidth: 100,
                      maxWidth: 200,
                      sortable: true
                    },
                    {
                      title: "Door No.",
                      key: "door",
                      align: "center",
                      minWidth: 100,
                      maxWidth: 200
                    }
                  ]
                }
              ]
            }
          ]
        },
        {
          title: "Company",
          align: "center",
          children: [
            {
              title: "Company Address",
              key: "caddress",
              align: "center",
              minWidth: 100,
              maxWidth: 200
            },
            {
              title: "Company Name",
              key: "cname",
              align: "center",
              minWidth: 100,
              maxWidth: 200
            }
          ]
        },
        // {
        //     title: 'Gender',
        //     key: 'gender',
        //     align: 'center',
        //     width: 200,
        //     fixed: 'right'
        // },
        {
          title: "Gender",
          key: "gender",
          align: "center",
          minWidth: 100,
          maxWidth: 200,
          fixed: "right"
        }
      ],
      columns2: [
        {
          title: "Name",
          key: "name",
          width: 100,
          fixed: "left"
        },
        {
          title: "Age",
          key: "age",
          width: 200,
          fixed: "left",
          sortable: true
        },
        {
          title: "Province",
          key: "province",
          width: 200
        },
        {
          title: "City",
          key: "city",
          width: 200
        },
        {
          title: "Address",
          key: "address",
          width: 200
        },
        {
          title: "Postcode",
          key: "zip",
          width: 200
        },
        {
          title: "Action",
          key: "action", 
          width: 120,
          render: (h, params) => {
            return h("div", [
              h(
                "Button",
                {
                  props: {
                    type: "text",
                    size: "small"
                  }
                },
                "View"
              ),
              h(
                "Button",
                {
                  props: {
                    type: "text",
                    size: "small"
                  }
                },
                "Edit"
              )
            ]);
          }
        }
      ],
      data1: [],
      data4: [
        {
          name: "John Brown",
          age: 18,
          address: "New York No. 1 Lake Park",
          province: "America",
          city: "New York",
          zip: 100000
        },
        {
          name: "Jim Green",
          age: 24,
          address: "Washington, D.C. No. 1 Lake Park",
          province: "America",
          city: "Washington, D.C.",
          zip: 100000
        },
        {
          name: "Joe Black",
          age: 30,
          address: "Sydney No. 1 Lake Park",
          province: "Australian",
          city: "Sydney",
          zip: 100000
        },
        {
          name: "Jon Snow",
          age: 26,
          address: "Ottawa No. 2 Lake Park",
          province: "Canada",
          city: "Ottawa",
          zip: 100000
        },
        {
          name: "John Brown",
          age: 18,
          address: "New York No. 1 Lake Park",
          province: "America",
          city: "New York",
          zip: 100000
        },
        {
          name: "Jim Green",
          age: 24,
          address: "Washington, D.C. No. 1 Lake Park",
          province: "America",
          city: "Washington, D.C.",
          zip: 100000
        },
        {
          name: "Joe Black",
          age: 30,
          address: "Sydney No. 1 Lake Park",
          province: "Australian",
          city: "Sydney",
          zip: 100000
        },
        {
          name: "Jon Snow",
          age: 26,
          address: "Ottawa No. 2 Lake Park",
          province: "Canada",
          city: "Ottawa",
          zip: 100000
        }
      ],
      columns5: [
        {
          title: "Date",
          key: "date",
          sortable: true
        },
        {
          title: "Name",
          key: "name"
        },
        {
          title: "Age",
          key: "age",
          sortable: true
        },
        {
          title: "Address",
          key: "address"
        }
      ],
      data5: [
        {
          name: "John Brown",
          age: 18,
          address: "New York No. 1 Lake Park",
          date: "2016-10-03"
        },
        {
          name: "Jim Green",
          age: 24,
          address: "London No. 1 Lake Park",
          date: "2016-10-01"
        },
        {
          name: "Joe Black",
          age: 30,
          address: "Sydney No. 1 Lake Park",
          date: "2016-10-02"
        },
        {
          name: "Jon Snow",
          age: 26,
          address: "Ottawa No. 2 Lake Park",
          date: "2016-10-04"
        }
      ],
      columns6: [
        {
          title: "Date",
          key: "date"
        },
        {
          title: "Name",
          key: "name"
        },
        {
          title: "Age",
          key: "age",
          filters: [
            {
              label: "Greater than 25",
              value: 1
            },
            {
              label: "Less than 25",
              value: 2
            }
          ],
          filterMultiple: false,
          filterMethod(value, row) {
            if (value === 1) {
              return row.age > 25;
            } else if (value === 2) {
              return row.age < 25;
            }
          }
        },
        {
          title: "Address",
          key: "address",
          fixed: "right",
          filters: [
            {
              label: "New York",
              value: "New York"
            },
            {
              label: "London",
              value: "London"
            },
            {
              label: "Sydney",
              value: "Sydney"
            }
          ],
          filterMethod(value, row) {
            return row.address.indexOf(value) > -1;
          }
        }
      ],

      columns7: [
        {
          title: "Date",
          key: "date",
          sortable: true,
          width: 200
        },
        {
          title: "Name",
          key: "name",
          width: 200
        },
        {
          title: "Age",
          key: "age",
          width: 200
        },
        {
          title: "Address",
          key: "address",
          width: 200
        }
      ],
      data7: [
        {
          name: "John Brown",
          age: 18,
          address: "New York No. 1 Lake Park",
          date: "2016-10-03"
        },
        {
          name: "Jim Green",
          age: 24,
          address: "London No. 1 Lake Park",
          date: "2016-10-01"
        },
        {
          name: "Joe Black",
          age: 30,
          address: "Sydney No. 1 Lake Park Sydney No. 1 Lake Park",
          date: "2016-10-02"
        },
        {
          name: "Jon Snow",
          age: 26,
          address:
            "Ottawa No. 2 Lake Park Ottawa No. 2 Lake Park Ottawa No. 2 Lake Park",
          date: "2016-10-04"
        }
      ],

      columns8: [
        {
          title: "Address",
          key: "address",
          minWidth: 200,
          fixed: "left"
          //maxWidth:300,
        },
        {
          title: "Date",
          key: "date",
          sortable: true,
          width: 300
        },
        {
          title: "Name",
          key: "name",
          minWidth: 300,
          maxWidth: 400
        },
        {
          title: "Age",
          key: "age",
          minWidth: 200,
          maxWidth: 300
        }
      ]
    };
  },
  mounted() {
    const data = [];
    for (let i = 0; i < 20; i++) {
      data.push({
        key: i,
        name: "John Brown",
        age: i + 1,
        street: "Lake Park",
        building: "C",
        door: 2035,
        caddress: "Lake Street 42",
        cname: "SoftLake Co",
        gender: "M"
      });
    }
    this.data1 = data;
    for (let i = 0; i < 20; i++) {
      this.data4.push({
        name: "Jon Snow",
        age: 26 + i,
        address: "Ottawa No. 2 Lake Park",
        province: "Canada",
        city: "Ottawa",
        zip: 100000
      });
    }
  },
  methods: {
    toggleCollapse() {
      this.$refs.side.toggleCollapse();
    },
    change() {
      this.isCollapsed = !this.isCollapsed;
    },
    changed(res) {
      console.log(res);
    }
  },
  watch: {
    isCollapsed(val) {
      // console.log(val)
    }
  }
};
</script>