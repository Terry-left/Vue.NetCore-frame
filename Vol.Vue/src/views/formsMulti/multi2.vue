<!--
*Author：jxx
 *Contact：283591387@qq.com
 *代码由框架生成,任何更改都可能导致被代码生成器覆盖
 *业务请在@/extension/order/App_Appointment.js此处编写
 -->
<template>
    <div>
        <view-grid :columns="columns"
                   :detail="detail"
                   :editFormFileds="editFormFileds"
                   :editFormOptions="editFormOptions"
                   :searchFormFileds="searchFormFileds"
                   :searchFormOptions="searchFormOptions"
                   :table="table"
                   :extend="extend">
        </view-grid>
    </div>
</template>

<script>
    import extend from "../formsMulti/multil2Extension/multi2.js"
    import ViewGrid from "@/components/basic/ViewGrid.vue";
    var vueParam = {
        components: {
            ViewGrid
        },
        data() {
            return {
                table: {
                    key: 'Id',
                    footer: "Foots",
                    cnName: '混合表单一对多',
                    name: 'App_Appointment',
                    url: "/App_Appointment/",
                    sortName: "CreateDate"
                },
                extend: extend,
                editFormFileds: {"Name":"","Id":"","Describe":"","PhoneNo":"","CreateDate":"","Creator":"","Modifier":"","ModifyDate":""},
                editFormOptions: [[{"columnType":"string","title":"姓名","required":true,"field":"Name","disabled":true},
                               {"columnType":"string","title":"","required":true,"field":"Id","disabled":true}],
                              [{"columnType":"string","title":"描述","required":true,"field":"Describe","disabled":true},
                               {"columnType":"string","title":"电话","required":true,"field":"PhoneNo","disabled":true}],
                              [{"columnType":"datetime","title":"创建时间","field":"CreateDate","disabled":true},
                               {"columnType":"string","title":"创建人","field":"Creator","disabled":true}],
                              [{"columnType":"string","title":"修改人","field":"Modifier","disabled":true},
                               {"columnType":"datetime","title":"修改时间","field":"ModifyDate","disabled":true}]],
                searchFormFileds: {"Name":"","PhoneNo":"","CreateDate":"","Creator":""},
                searchFormOptions: [[{"columnType":"string","title":"姓名","field":"Name"},{"columnType":"string","title":"电话","field":"PhoneNo"},{"columnType":"datetime","title":"创建时间","field":"CreateDate","type":"datetime"},{"columnType":"string","title":"创建人","field":"Creator"}]],
                columns: [{field:'Name',title:'姓名',type:'string',link:true,width:100,readonly:true,require:true,align:'left',sortable:true},
                       {field:'Describe',title:'描述',type:'string',width:180,readonly:true,require:true,align:'left'},
                       {field:'PhoneNo',title:'电话',type:'string',width:130,readonly:true,require:true,align:'left'},
                       {field:'Id',title:'Id',type:'string',width:90,hidden:true,readonly:true,require:true,align:'left'},
                       {field:'CreateDate',title:'创建时间',type:'datetime',width:120,readonly:true,align:'left',sortable:true},
                       {field:'CreateID',title:'CreateID',type:'int',width:80,hidden:true,align:'left'},
                       {field:'Creator',title:'创建人',type:'string',width:130,readonly:true,align:'left'},
                       {field:'Modifier',title:'修改人',type:'string',width:130,readonly:true,align:'left'},
                       {field:'ModifyDate',title:'修改时间',type:'datetime',width:90,readonly:true,align:'left',sortable:true},
                       {field:'ModifyID',title:'ModifyID',type:'int',width:80,hidden:true,align:'left'}],
                detail: {
                    cnName:"#detailCnName",
                    columns: [],
                    sortName: "",
                    key:""
                }
            };
        }
    };
    export default vueParam;
</script>
