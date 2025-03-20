# Blockchain-Based Document Verification Platform

![1](https://github.com/user-attachments/assets/b600bb22-7502-4b7c-a3a7-40133818b007)
![4](https://github.com/user-attachments/assets/72d3c015-36a1-4a52-83b6-aa99f67544e2)
![5](https://github.com/user-attachments/assets/af5103b1-097f-4045-81bb-2365a516ac2d)
![6](https://github.com/user-attachments/assets/f7710a50-1a22-4a6f-aa95-f63abcb3245c)
![7](https://github.com/user-attachments/assets/5f97048b-6c37-4616-a1d5-b2aacc235449)
![8](https://github.com/user-attachments/assets/49d97c6a-0f35-4bd3-a266-aa0caa37cd5c)


## Overview
This project is a blockchain-based document verification platform that leverages Ethereum to store and verify documents such as NTA results, RTO driving licenses, course certificates, and university result cards. The platform integrates with Aadhaar for identity verification and ensures that data is stored securely on-chain, making documents tamper-proof and verifiable by authorized parties.

The platform features two main functionalities:
1. **Certificate Creation and Management** – For institutions to create and manage certificates.
2. **Document Verification** – For authorized government personnel to verify the authenticity of documents submitted by users.

## Table of Contents
1. [Overview](#overview)
2. [Portals and Functionalities](#portals-and-functionalities)
   - [Admin Portal](#admin-portal)
   - [Verifier Portal](#verifier-portal)
3. [Technologies Used](#technologies-used)
4. [Challenges Faced](#challenges-faced)
5. [How It Fits Into ETHIndia: Ethereum Track](#how-it-fits-into-ethindia-ethereum-track)

## Portals and Functionalities

### Admin Portal
The Admin Portal is used by institutions to create, manage, and issue certificates. It includes the following functionalities:

- **Login**: Institutions log in using a unique login ID provided for secure access.
- **Certificate Creation**: Admins can create certificates linked to a user's Aadhaar number. This ensures authenticity by associating each certificate with a verified identity.
- **View Previous Certificates**: Admins can view and verify previously created certificates associated with a particular Aadhaar number, ensuring there are no duplicates or fraudulent entries.
- **Download and Confirmation**: After creating a certificate, the institution can download it, view details, and confirm its validity.
- **Aadhaar Integration**: The platform fetches data from the Aadhaar system during certificate creation, ensuring the data matches the verified identity.

### Verifier Portal
The Verifier Portal is designed for authorized government personnel and includes these functionalities :

- **Secure Login and Signup**: Only government-verified entities can access this portal. Each verifier must authenticate their identity to gain access.
- **Document Verification**: Verifiers can upload a PDF of the certificate they wish to verify. The system checks if the document matches the on-chain data.
- **Tamper Detection**: If a certificate's details have been altered, the platform identifies changes through hash comparison and flags the document as tampered.
- **Genuine Document Confirmation**: If the document matches the on-chain data and hash values, the system confirms its authenticity and marks it as genuine.

## Technologies Used
Ethereum, Solidity, IPFS, Node.js, React, Aadhaar API, Web3.js, OAuth, IPFS, Metamask

## Challenges Faced
1. **Aadhaar Integration**: Implementing secure and compliant data fetching from Aadhaar was challenging. We used encryption and multi-factor authentication to protect data access.
2. **On-Chain Data Storage**: Storing data on-chain while optimizing gas fees required a balance between what is stored directly on the blockchain and what is stored on IPFS.
3. **Hash-Based Verification**: Developing a reliable mechanism to detect document tampering through hash value changes took extensive testing and fine-tuning.
4. **Role-Based Access Management**: Securing access to the Verifier Portal required careful implementation of role-based access control using OAuth.

## How It Fits Into ETHIndia: Ethereum Track
Our project uses Ethereum’s blockchain to create a secure, tamper-proof, and transparent document verification system. By storing certificate data on-chain and using smart contracts to automate the verification process, we demonstrate the potential of Ethereum for solving real-world problems. The platform aligns with the Ethereum ethos of decentralization, security, and transparency, making it an ideal fit for ETHIndia: Ethereum Track.

