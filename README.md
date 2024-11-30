# Solana-Vanity-Generator

## Example

```
import { generateVanityAddress } from "./vanityAddress"; 


let counter = 0;
const incrementCounter = () => {
  counter++;
  console.log(`conter: ${counter}`);
}


const prefix = "Sol";
const suffix = "123";
const caseSensitive = false;


const keypair = generateVanityAddress(prefix, suffix, caseSensitive, incrementCounter);

console.log("address:");
console.log("Pubkey:", keypair.publicKey.toBase58());
console.log("private key:", keypair.secretKey.toString());

```

# Solana Vanity Generator

Solana Vanity Generator is a tool for generating Solana addresses that meet specific prefix and suffix requirements. With this tool, developers can create customized "vanity" Solana addresses to meet the personalized needs of blockchain applications. It supports flexible prefix and suffix configurations and allows customization of case sensitivity.

## Features

**Customizable Prefix and Suffix:** The generated Solana address can have custom prefixes and suffixes to meet specific naming requirements.

**Case Sensitivity:**  Supports case sensitivity, ensuring the address fully matches the desired format.

**Efficient Generation:**  Continuously tries generating new addresses until one that meets the criteria is found.

**Simple and Easy to Use:**  Easy to integrate into Solana-based projects, with the ability to call a callback function to track the generation process.
