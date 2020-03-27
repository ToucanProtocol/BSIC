# Deliverable 3: Proof-of-Concept & MVP Testing Approach

> ## Prototype your solution in some manner
> * *Working code*
> * *Analog prototype / mockups*
> * *Tech stack and wireframes*
> ## Define your Minimum Viable Product (MVP) testing approach
> * Marketing tests: landing page, explainer video, ad campaign, A/B Tests, crowdfunding
> * Product tests: sketches, wireframes, mockups, interactive prototype, Wizard of Oz, Concierge, live product
> ## End of Week Deliverables
> * Prototype /proof-of-concept uploaded
> * Document defining your MVP testing approach  


## Prototype
### Project architecture
The figure below shows the architecture of the project. For a detailed description and an overall project overview please refer to this [Medium post](https://medium.com/curve-labs/co2ken-genesis-74d7a1387ea1) and [this PDF](https://github.com/CO2ken/BSCI/blob/master/Deliverable%20%233/Architecutre%20overview.pdf).

![Architecture](https://github.com/CO2ken/CO2ken/blob/master/Presentation/Illustrations/DAO2architecture6.png)

### Code deliverables

For the prototype we have built the following elements:
1. **The DAO**
    * We have deployed a DAO with the DAOStack framework on the Rinkeby network which you can find [here](https://alchemy-staging-rinkeby.herokuapp.com/dao/0xe953b4706b66d4f34100ccc5e3ef5dc8acc5e775)
    * We have built a custom scheme (plugin) for Alchemy to be able to interact with our [`CO2ken.sol`](https://github.com/CO2ken/CO2ken/blob/master/Contracts/co2ken.sol) contract. 
        * The process for setting up this scheme is described [here](https://github.com/CO2ken/CO2ken/blob/master/DAO/DAOStack%20setup/setup.md)
        * The scheme is found [here](https://github.com/CO2ken/CO2ken/blob/master/DAO/DAOStack%20setup/CO2ken.json)
        * The custom Alchemy UI can be found [here](https://github.com/CO2ken/alchemy)
    
2. **The Smart Contracts**
    * All contracts can be found in [this folder](https://github.com/CO2ken/CO2ken/tree/master/Contracts)
    * The `co2ken.sol` contract is the main token contract
    * The `green.sol` contract contains the Solidity modifier which allows other contracts to automatically offset their emissions
    * The `co2kenData.sol` contract is a data storage contract accessed by the other two contracts above

3. **The API**
    * We have deployed an API called `eth-co2.js` which makes it easy for all dApps to interact with our smart contracts
    * The repo containing the code can be found [here](https://github.com/CO2ken/eth-co2)
    * The published npm package can be found [here](https://www.npmjs.com/package/eth-co2)

4. **The Frontend / UI**
    * We've deployed a simple web3 app at www.co2ken.io which is using our **API** to connect to our smart contracts
    * The backend code for this can be found [here](https://github.com/CO2ken/demo-frontend/tree/master/webflow)
    * We've deployed a simple web3 app called *Polluter* to demonstrate the functionality of the Solidity modifier. It can be found at https://polluter.co2ken.io/
    * The code for the polluter page can be found [here](https://github.com/CO2ken/demo-frontend/tree/master/polluter)

* * *

## MVP Testing Approach

Based on our **user persona** research (figure below), we have identified *Dani* as the core customer we want to reach with our *MVP*. 

![User Persona](https://github.com/CO2ken/BSCI/blob/master/Deliverable%20%233/User%20Persona.jpg)

Since our project involves a lot of stakeholders which are not necessarily suppliers or customers, we've made a stakeholder map to have a better overview:

![Stakeholder Map](https://github.com/CO2ken/BSCI/blob/master/Deliverable%20%233/Stakeholder%20Map.jpg)

We then looked at the **Business Model Canvas** for *Phase 0: MVP*:

![User Persona](https://github.com/CO2ken/BSCI/blob/master/Deliverable%20%233/MVP%20Business%20Model%20Canvas.jpg)

We then formulated 3 tests to validate the success of our MVP:
1. *Are people interested in buying tokenized carbon offsets?*  
    **Validation:** 40 users (like *Dani*) buy CO2kens via our UI.

2. *Are investors interested in founding this project?*  
    **Validation:** 1 fund reaching out (unsolicited) with the objective to invest.

3. *Are carbon offset projects interested in joining a CarbonDAO?*  
    **Validation:** contact 10 projects with at least 3 positive replies.

![MVP Testing Approach](https://github.com/CO2ken/BSCI/blob/master/Deliverable%20%233/MVP%20Testing%20Approach.jpg)
