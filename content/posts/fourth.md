---
title: "SDK + Token bound account integrate"
date: 2023-08-10T15:31:44-06:00
draft: false
ShowToc: true
updated: 2023-08-24
# cover: 
#     image: "img/wall.jpg"
#     alt: "This is a photo."
#     caption: "This is the caption."
---
# Backend API Documentation

This document provides **technical** documentation for the backend API of your application and can go in-depth. In case of looking for a quickstart, look at our [SDK + React guide]({{< ref "react" >}}).

The backend is developed using Node.js and Express framework, and it comprises various routes that handle different functionalities such as user management, wallet operations, application handling, authentication, and more.

## **Introduction**

The backend API plays a pivotal role in the functionality and success of your application. It's designed to seamlessly handle various crucial tasks such as managing users, facilitating wallet operations, handling applications, enabling secure authentication, and more. To streamline these operations and provide enhanced features, your backend leverages the power of the **`@dippixyz/sdk`** library.

### **The Power of `@dippixyz/sdk`**

One of the core strengths of this backend lies in its integration with the **`@dippixyz/sdk`** library. This SDK offers a comprehensive set of tools and functionalities that empower your backend to interact seamlessly with the Dippi platform. By leveraging the capabilities of the **`@dippixyz/sdk`**, your backend gains access to a wealth of features that simplify application management, user authentication, wallet handling, and more.

The **`@dippixyz/sdk`** library serves as the bridge between your backend and the Dippi ecosystem. It encapsulates intricate processes, allowing you to focus on building an efficient and feature-rich backend without the need to handle intricate details manually. With the power of the SDK, your backend can execute actions smoothly and securely, offering a seamless experience to your users.

## Table of Contents

- [Introduction](notion://www.notion.so/dippi/94e479b4a0db4a6782a4ea94fb2bfeaf?v=5701ff4bdd01486389c0c66d36e7ccb3&p=75d17264668e48e6a61ae9681a8b236c&pm=s#introduction)
- [Routes](notion://www.notion.so/dippi/94e479b4a0db4a6782a4ea94fb2bfeaf?v=5701ff4bdd01486389c0c66d36e7ccb3&p=75d17264668e48e6a61ae9681a8b236c&pm=s#routes)
    - [TokenAccountFunc Router](notion://www.notion.so/dippi/94e479b4a0db4a6782a4ea94fb2bfeaf?v=5701ff4bdd01486389c0c66d36e7ccb3&p=75d17264668e48e6a61ae9681a8b236c&pm=s#TokenAccountFunc-router)
    
- [Models](notion://www.notion.so/dippi/94e479b4a0db4a6782a4ea94fb2bfeaf?v=5701ff4bdd01486389c0c66d36e7ccb3&p=75d17264668e48e6a61ae9681a8b236c&pm=s#models)

## Introduction

The backend API is responsible for handling various functionalities of your application. It is built using Node.js and Express, providing a set of routes that interact with different models to manage users, wallets, applications, authentication, and more.

## Routes

### TokenAccountFunc Router

The `tokenBoundAccount-router.js` manages wallet operations.

- `POST /dippi/tokenBoundAccount/create`: Create 6551.


## Models


### tokenBoundAccount Model

The `tokenBoundAccount.js` file provides methods to interact with tokenBoundAccount-related operations using the Dippi SDK.

### Method: create

```jsx
const TBA = require('@dippixyz/sdk');

const create = async (data) => {
    const TBAClient = new TBA(paramsOauthSession);
    TBAClient.init(tbaCreateOptions)
    return await TBAClient.create();
}

module.exports = {
    create,
};

```