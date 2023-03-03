<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import { EthereumPrivateKeyProvider } from "@web3auth/ethereum-provider"

const ethereumPrivateKeyProvider = new EthereumPrivateKeyProvider({
			  config: {
				/*
				pass the chain config that you want to connect with
				all chainConfig fields are required.
				*/
				chainConfig: {
				  chainId: "0x13881",
				  rpcTarget: "https://rpc.ankr.com/polygon_mumbai",
				  displayName: "Polygon Testnet",
				  blockExplorer: "https://mumbai.polygonscan.com",
				  ticker: "MATIC",
				  tickerName: "Matic",
				},
			  },
			});

console.log(ethereumPrivateKeyProvider)

</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
