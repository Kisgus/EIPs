
## Linkdrop Protocol

### Team members 

Mikhail Dobrokhvalov,
Dev lead,
https://github.com/Dobrokhvalov

Gustav Friis,
Biz lead,
https://www.linkedin.com/in/gustav-friis-20201086/

Artyom Ignatyev,
Product lead,
https://www.linkedin.com/in/artyomignatyev

Amirkhon Jumaniyazov,
Backend dev,
https://github.com/amiromayer

Haz,
Frontend dev,
https://github.com/spacehaz


### What project are you building 

**General description**

[Linkdrop](https://linkdrop.org/) is an open protocol for including digital assets and onboarding properties into links and QR codes. 
This allows non-crypto users to simply click a URL or scan a linkdrop QR code to get onboarded. Place check out our already live [mainnet demo applications](https://linkdrop.org/demo/) to see how this looks like for one-to-many and one-to-one linkdrops.

**GECO specific**

We wish to developer a full meta-linkdrop implementation in order to extend linkdrop functionality to Gnosis Safe

### Why did you decide to build it 

Our general motivation for working on the Linkdrop Protocol is that we see usability of web3 being a major blocker for mainstream adoption in an equivalent manner to scalability.
On the specific topic of meta-linkdrops we initially met and won two first prizes at the Status Hackathon by enabling to include [Universal Login Identity Contracts paired with ENS](https://www.youtube.com/watch?v=K67dOixMBWI) into shareable URLs.
We seet his meta-linkdrop module is a very useful feature to include in the wallet contract of the Gnosis Safe.

### How long will it take 

The entire  [linkdrop protocol roadmap](https://github.com/LinkdropProtocol/Proposal-Paper/blob/master/README.md) spands over 2019.
The specific meta-linkdrop implementation is estimated to spand over Q2 and Q3 of 2019.

### How much funding are you requesting  
We are requesting 50k to develop the generalized meta-linkdrop SDK as well as and provide an end-to-end working solution for the Gnosis Safe

### How did you hear about the GECO

Through whispers in the full node office

## Your Proposal 
### Project description

We drafted below meta-linkdrop scheme to work with Universal Login SDK
and already developed this gass-less webwallet implementation to enable

### Assumptions

In order for the invite functionality scheme to work in practice, the following assumptions needs to be valid: 

- Alice has an EIP 1078 identity contract and wants to send an ERC721 or ERC20 token to Bob
- Bob is a new user without ETH, wallet or any prior crypto knowledge
- Alice share the QR code or invite link with Bob over a secure channel e.g Signal
- There is a proper incentive in place (on a user, dapp or relay level) to pay gas

### Key Scheme

![invite scheme](https://user-images.githubusercontent.com/18598519/48316096-10f8ab00-e5df-11e8-89f0-63a0397c904c.png)

1. Alice shares an invite link or QR code with Bob, including a transit private key and a signature
1. Clicking the link, Bob is directed to a webpage
2. Bob generates his own private key stored in the browser
3. Bob uses the transit private key to sign Bob’s address
4. Bob’s browser sends his two signatures to the relayer 
5. The Relayer calls Alice’s identity contract
6. Then Alice’s identity contract creates an identity contract for Bob and sends a Robot
7. In addition, Bob can now also help Alice recover access to her identity contract in the future using a social key recovery mechanism
8. Bob now got the Robot he wanted, and in addition has a Universal Login Contract and ENS name 9. which allows him to use the best of web3 to login to all other Ethereum dapps.

## Rationale

The rationale for above is enabling to send digital assets and/or Universal Login invite link to users before they have any Ethereum address yet. This will enable new users to get onboarded to the entire dapp ecosystem by only clicking a link or scanning a QR code.


### Features
_How do you plan to implement your project, which tools and framework will you use? Optional: Architecture, Mockups, etc._
### Team description
_Who are your team members, what is your background and what you built before._
### Timeline, Milestones and Deliverables
_Detailed description of your timeline milestones and the corresponding payouts_

**Phase I**  			_Outline the different phases_

**Deliverables** 			_What features will be implemented_

**Time and Price Estimate**	_How long will it take and what is the estimated price_

**Phase II**  			_Outline the different phases_

**Deliverables** 			_What features will be implemented_

**Time and Price Estimate**	_How long will it take and what is the estimated price_

**Phase III**  			_..._


### Others	 
Anything else you want to share with us
