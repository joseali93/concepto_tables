<template>
  <div>
    <h6>Left alignment (default)</h6>
    
    <br>
    <div>currentPage: {{currentPage}}</div>
<div>
<b-table
             :items="items"
             :fields="fields"
             :per-page="2"
             :current-page="currentPage">
             
    </b-table>
    <b-pagination :total-rows="items.length" v-model="currentPage" :per-page="2">
    </b-pagination>
</div>
  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
export default {
  data () {
    return {
      currentPage: 1,
      fields: [
        { key: 'last_name', sortable: false },
        { key: 'first_name.name', sortable: false },
        { key: 'age', sortable: false },
        { key: 'isActive', sortable: false }
      ],
      items: [
        { isActive: true, age: 40, first_name: {name:'Dickerson'}, last_name: 'Macdonald' },
        { isActive: false, age: 21, first_name: {name:'Larsen'}, last_name: 'Shaw' },
        { isActive: false, age: 89, first_name: {name:'Geneva'}, last_name: 'Wilson' },
        { isActive: false, age: 89, first_name: {name:'Geneva'}, last_name: 'Wilfson' },
        { isActive: false, age: 89, first_name: {name:'Geneva'}, last_name: 'Wislson' },
        { isActive: false, age: 89, first_name: {name:'Geneva'}, last_name: 'Wilssdadn' },
      ]

    }
  }
}
</script>

<!-- pagination-2.vue -->