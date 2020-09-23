<template>
  <div>
    <h1>{{ title }}</h1>
    <ul>

      <book-item v-for="book in books" :book="book">
      <!-- Display book items and insert book as props -->
      </book-item>
    </ul>
  </div>
</template>
<script>

  import BookItem from './BookItem';

  export default {
    name: 'BookList',
    data() {
      return {
        title: "All Books",
        books: [
          { title: 'Self-Reliance', author: 'Ralph Waldo Emerson'},
          { title: 'American Gods', author: 'Neil Gaiman'},
          { title: 'Amusing Ourselves to Death', author: 'Neil Postman'},
        ],
      }
    },
    components: {
      BookItem
    }

  };

</script>
<style>

  ul {
    list-style-type: none;
    padding: 0;
  }
  h1, h2 {
    font-weight: normal;
  }

</style>
