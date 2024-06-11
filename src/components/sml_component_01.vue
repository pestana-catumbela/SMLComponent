<script setup>
  const control = true;
</script>

<template>
  <div class="component1">
    <div class="component1__top">
      <div class="component1__top-icon">
        <img src="../assets/File upload icon.png" alt="File Icon" v-if="control" />
        <img src="../assets/File upload icon-2.png" alt="File Icon" v-else= />
      </div>

      <div class="component1__top-text">
          <h3>Tech design requirements.pdf</h3>
          <p>A Alguns segundos atrás - Bruno Delorence</p>
      </div>

      <div class="component1__top-loading" v-if="control">
        <div class="load"></div>
      </div>
      <div class="component1__top-loading" v-else>
        <div class="circle"></div>
      </div>
    </div>

    <div class="component1__bottom">
      <span class="component1__bottom-true" v-if="control">Processando</span>
      <span class="component1__bottom-false" v-else>Tentar novamente</span>
    </div>
  </div>
</template>

<style scoped>
  .component1 {
    width: 370px;
    padding: 14px;
    border: 1px solid red;
  }

  .component1__top {
    display: flex;
    justify-content: space-between;
    border-bottom: 1px solid #ccc;
    margin: 0px 0px 7px 0px;
  }

  .component1__top-text {
    
  }

  .component1__top-text > h3 {
    margin: 0;
    padding: 0;
    color: #333;
    font-size: 15px;
  }

  .component1__top-text > p {
    margin: 16px 0 10px 0;
    padding: 0;
    color: #333;
    font-size: 13px;
  }

  .component1__top-loading {
    font-size: 10px;
  }

  .load {
    animation: is-rotating 1s infinite;
    border: 3px solid #e5e5e5;
    border-radius: 50%;
    border-top-color: #30449e;
    height: 10px;
    width: 10px;
  }

  @keyframes is-rotating {
    to {
      transform: rotate(1turn);
    }
  }

  .circle {
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background-color: #b34040;
  }

  .component1__bottom {
    display: flex;
    justify-content: end;
  }

  .component1__bottom-true {
    color: #333;
    font-size: 14px;
    font-weight: 600;
  }

  .component1__bottom-false {
    color: #b34040;
    font-size: 14px;
    font-weight: 600;
  }
</style>