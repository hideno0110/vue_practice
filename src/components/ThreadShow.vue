<template>
  <div>
    <h1>hello vue.js</h1>
    <div class="col-large push-top">
      <h1>{{thread.title}}</h1>
      <div class="post-list">
        <div v-for="postId in thread.posts" class="post">
          <div class="user-info">
            <a href="#" class="user-name">{{users[posts[postId].userId].name}}
            </a>
            <img class="avatar-large" :src="users[posts[postId].userId].avatar" alt="">
          </div>
          <div class="post-content">
            <p>{{posts[postId].text}}</p>
          </div>
        </div>
      </div>

    </div>
  </div>

</template>

<script>
  export default {
    props: {
      id: {
        required: true,
        type: String
      }
    }
  }
</script>
