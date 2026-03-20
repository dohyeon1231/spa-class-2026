<script setup>
import { ref } from 'vue' 

const userInfo = ref({
  username: '',
  gender: 'male',
  hobbies: []
})
</script>

<template>
  <div class="container">
    <h2>📝 실시간 회원가입 폼</h2>

    <div class="field">
      <label>이름: </label>
      <input type="text" v-model="userInfo.username" placeholder="이름을 입력하세요">
    </div>

    <div class="field">
      <label>성별: </label>
      <label><input type="radio" value="male" v-model="userInfo.gender"> 남성</label>
      <label><input type="radio" value="female" v-model="userInfo.gender"> 여성</label>
    </div>

    <div class="field">
      <label>취미: </label>
      <label><input type="checkbox" value="코딩" v-model="userInfo.hobbies"> 코딩</label>
      <label><input type="checkbox" value="영화" v-model="userInfo.hobbies"> 영화</label>
      <label><input type="checkbox" value="게임" v-model="userInfo.hobbies"> 게임</label>
    </div>

    <hr>
    <h3>실시간 데이터 반영 결과:</h3>
    <pre class="result-box">{{ userInfo }}</pre>
  </div>
</template>

<style scoped>

.container {
  background-color: #1a1d23; 
  color: #ffffff; 
  padding: 40px;
  font-family: 'Pretendard', sans-serif;
  max-width: 500px;
  margin: 50px auto;
  border-radius: 20px;
  
  
  border: 2px solid #52e5a4;
  box-shadow: 0 0 20px rgba(82, 229, 164, 0.3);
}

h2 {
  margin-top: 0;
  font-size: 1.5rem;
  border-bottom: 1px solid #333;
  padding-bottom: 20px;
}


.field {
  margin-bottom: 25px;
}

input[type="text"] {
  background: #2c313a;
  border: 1px solid #444;
  color: white;
  padding: 10px 15px;
  border-radius: 8px;
  width: 100%;
  box-sizing: border-box;
  margin-top: 8px;
}

input[type="text"]:focus {
  outline: none;
  border-color: #52e5a4; 
}


label {
  margin-right: 15px;
  cursor: pointer;
  font-size: 0.95rem;
}


.result-box {
  background: #282c34;
  color: #abb2bf;
  padding: 20px;
  border-radius: 12px;
  font-weight: 500;
  line-height: 1.6;
  border: 1px solid #52e5a4; 
  overflow-x: auto;
}

hr {
  border: 0;
  border-top: 1px solid #333;
  margin: 30px 0;
}
</style>