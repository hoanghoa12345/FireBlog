<template>
  <div class="home">
    <blog-post :post="welcomeScreen" />
    <blog-post :post="post" v-for="(post, index) in sampleBlogPost" :key="index" />
  </div>
</template>

<script>
//https://youtu.be/ISv22NNL-aE?t=3898
import BlogPost from '../components/BlogPost.vue';
export default {
  name: "Home",
  components: {BlogPost},
  data() {
    return {
      welcomeScreen: {
        title: "Welcome!",
        blogPost:
          "Weekly blog articles with all things programming including HTML, CSS, JavaScript and more. Register today to never miss a post!",
        welcomeScreen: true,
        photo: "coding",
      },
      sampleBlogPost: [
        {
          title: "This is a Filler Title!",
          blogHTML: "This is a filler blog post title!",
          blogCoverPhoto: "beatiful-stories"
        },
        {
          title: "This is a post 2",
          blogHTML: "This is a post 2",
          blogCoverPhoto: "designed-for-everyone"
        }
      ]
    }
  }
};
</script>
