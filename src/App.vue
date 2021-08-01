<template>
  <div @click="increase">
    {{ count }}
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() { //여기서 정의한 변수는 반응성을 가지지 않음
    let count = ref(0) // 반응성을 가진 객체 데이터로 만들어줌
    function increase() {
      count.value += 1 //객체가 되었기 때문에 value로 접근
    }

    return {
      count,
      increase
    }
  }
}
</script>