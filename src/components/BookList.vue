<template>
    <div>
        <h1>{{title}}</h1>
        <ul>
          <!-- <li>LOTR - Fellowship Of The Ring</li>
          <li>LOTR - The Two Towers</li>
          <li>LOTR - The Return Of The King</li> -->
          <li v-for="book in books" :book=book></li>
        </ul>
    </div>
</template>
<script>
    import BookItem from './BookItem.vue'
    export default {
      name: "BookList",
      data() {
        return
        {
          title:"All Books",
          books: [
              {title: 'Self-Reliance', author: 'Ralph Waldo Emerson'},
              {title: 'American Gods', author: 'Neil Gaiman'},
              {title: 'Amusing Ourselves to Death', author: 'Neil Postman'},
          ]
        }
      },
      components: { BookItem }
    }
</script>
<style>
    h1, h2 {
        font-weight: normal;
    }

    ul {
      list-style-type: none;
      padding:0;
    }
</style>
