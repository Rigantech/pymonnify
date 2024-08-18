# pymonnify

`pymonnify` is a Python library that simplifies the interaction with the Monnify payment gateway. This library wraps around the Monnify API, allowing users to make **GET** and **POST** requests to various Monnify endpoints with ease, without needing to handle the complexities of crafting HTTP requests.

## Features
- Simple and intuitive interface for interacting with Monnify's API.
- Functions to perform common operations such as checking wallet balance, initiating transactions, and more.
- Easily extendable to add more endpoints as Monnify evolves.

## Registration
To use this library effectively, ensure you have created an account with monnify. if not, kindly create an account here [https://app.monnify.com/create-account](https://app.monnify.com/create-account)

## Installation

You can install this library using pip (once it's published):
```bash
pip install pymonnify
```

## Usage
### Basic setup

First, you'll need to create an instance of the Monnify class by passing your contract code and wallet account number:
```python
from pymonnify import Monnify

# Initialize the Monnify class with your API key, Client Secret Key and Environment
monnify = Monnify(apiKey="your_api_key", clientSecretKey="your_client_secret_key", environment="live")
# environment can either be "live" for production or "sandbox" for development.
# If no environment is specified, it defaults to "live"
```

### Available Functions

<table>
    <thead>
        <tr>
            <th>Category</th>
            <th>Functions</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Reserved Accounts</td>
            <td>
                <ul>
                    <li>Create Reserved Account (Invoice)</li>
                    <li>Create Reserved Account (General)</li>
                    <li>Get Reserved Account Details</li>
                    <li>Delete Reserved Accounts</li>
                    <li>Add Linked Accounts</li>
                    <li>Update BVN for Reserved Account</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Transactions</td>
            <td>
                <ul>
                    <li>Initiate A Transaction</li>
                    <li>Pay With Bank Transfer</li>
                    <li>Pay With Card</li>
                    <li>Authroize OTP</li>
                    <li>Get Transactions For A Reserved Account</li>
                    <li>Get All Transactions / Search Transactions</li>
                    <li>Get A Transaction Details</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Sub Accounts</td>
            <td>
                <ul>
                    <li>Create Sub Account</li>
                    <li>Delete Sub Account</li>
                    <li>Get All Sub Accounts</li>
                    <li>Update A Sub Account Info</li>
                    <li>Update Split Config For A Reserved Account</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Transfers</td>
            <td>
                <ul>
                    <li>Initiate A Single Transfer</li>
                    <li>Authorize A Transfer / Validate OTP</li>
                    <li>Resend OTP</li>
                    <li>Get Transfer Status</li>
                    <li>Search Transfers</li>
                    <li>Get All Transfers</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Wallet Account</td>
            <td>
                <ul>
                    <li>Get Wallet Balance</li>
                    <li>Get List of Banks (supported by Monnify) <a href="./src/assets/banks.json">See sample list</a></li>
                    <li>Get All Available Bank USSDs (supported by Monnify) <a href="./src/assets/banks_ussd.json">See sample list</a></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Bank Verification</td>
            <td>
                <ul>
                    <li>Verify Bank Account</li>
                    <li>Verify BVN Number (with Date of Birth)</li>
                    <li>Verify BVN Number (with Bank Account)</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>WebHooks</td>
            <td>
                <ul>
                    <li>Check Verified Valid Payment</li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>

### Usage
[See Documentation Here](https://hackode-doc-whizzydocs-projects.vercel.app/) for how to use the functions