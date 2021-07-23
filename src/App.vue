<template>
  <div class="ctr">
    <question
      v-if="questionsAnswered < questions.length"
      :questions="questions"
    />
    <result v-else />
    <button type="button" class="reset-btn">Reset</button>
  </div>
</template>

<script>
import Question from "./components/Question.vue";
import Result from "./components/Result.vue";
import data from "./assets/data.json";
export default {
  name: "App",
  components: {
    Question,
    Result,
  },
  data() {
    return {
      questionsAnswered: 0,
      questions: data.questions,
      results: data.results,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
