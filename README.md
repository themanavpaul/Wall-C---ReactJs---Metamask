# Lets see what are we building here

Live Website: [Wall C](https://wallc.netlify.app/)

# Get started with Creating React Application


## Step 1: Creating a react project with CLI

```
npx create-react-app eth_app
or
yarn create react-app eth_app

```

### Move into Project Directory

```
cd eth_app
```



### **Installing ether.js**

```
npm install --save ethers
```



### **Installing react bootstrap validation**

```
npm install react-bootstrap-validation --save
```



### **Install bootstrap**

```
npm i bootstrap
```


## Step 2: Connecting Metamask to react app. 

For achieving the meta mask wallet address we need to connect MetaMaks to our react app. For checking, if meta mask is connected.

```
if(window.ethereum){
      // Do something 
    }else{
      alert("install metamask extension!!")
    }
Now, if meta mask is installed we need to request the account.

window.ethereum.request({method:'eth_requestAccounts'})
.then(res=>{
        // Return the address of the wallet
        console.log(res) 
})
```

**For getting the balance we need to request the balance method**

```
window.ethereum.request({
    method:'eth_getBalance', 
    params: [address, 'latest']
}).then(balance => {
    // Return string value to convert it into int balance
    console.log(balance) 
      
    // Yarn add ethers for using ethers utils or
    // npm install ethers
    console.log(ethers.utils.formatEther(balance))
    // Format the string into main latest balance
})
```

## Step 3: Fetch Data to React
 
For fetching the information into react page, we will use useState for setting the value from the javascript method and using into jsx

 ```
const [data, setdata] = useState({
    address:'',    // Stores address
    Balance: null  // Stores balance
  })
```

App.css file is optional for dapp layout

