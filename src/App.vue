<template>
  <h1>{{ title }}</h1>
  <p>Welcome</p>
  <div v-if="showModal">
    <Modal theme="sale" @close="toggleModal">
      <template v-slot:links>
        <a href="#">sign up now</a>
        <a href="#">more info</a>
      </template>
      <h1>Ninja Givaway!</h1>
      <p>Grab your ninja swag for half price!</p>
    </Modal>
  </div>
  <button @click="toggleModal">Open Modal</button>
  <div v-if="showModal2">
    <Modal @close="toggleModal2">
      <template v-slot:links>
        <a href="#">Take part in the giveaway!!</a>
      </template>
      <h1>Brand new NFT pre-launch giveaway!!</h1>
      <p>Get an NFT for free before the launch of the new NFT token!</p>
    </Modal>
  </div>
  <button @click="toggleModal2">Open Modal 2</button>
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "App",
  components: {
    Modal,
  },
  data() {
    return {
      title: "My First Vue App",
      showModal: false,
      showModal2: false,
    };
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },
    toggleModal2() {
      this.showModal2 = !this.showModal2;
    },
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
h1 {
  color: blueviolet;
}
</style>
