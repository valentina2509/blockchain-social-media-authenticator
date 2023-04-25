# blockchain-social-media-authenticator

A Social Media Authenticator using Blockchain

This project is a blockchain-based social media authentication system. It uses blind signatures to provide a secure and private authentication mechanism.

The system consists of a blockchain node that handles user registration, login, and authentication. When a user registers, their password is hashed and salted and stored in a database. When a user logs in, their password is hashed and compared to the hash stored in the database. If the hashes match, the user is authenticated.

The system also supports blind signatures, which allow users to authenticate without revealing their passwords. When a user requests a blind signature, the blockchain node generates a key pair and uses the user's message to create a hash. The hash is then signed using the private key and returned to the user along with the public key. The user can then use the blind signature to authenticate without revealing their message or private key.

Installation

To install the project, follow these steps:

Clone the repository: git clone https://github.com/valentina2509/blockchain-social-media-authenticator.git

Install the dependencies: pip install -r requirements.txt OR pip3 install -r requirements.txt

Configure the system: cp config.example.py config.py and modify config.py as needed

Run the system: python main.py OR python3 main.py


Usage

To use the system, you can interact with it using HTTP requests. The following endpoints are available:

POST /register: Register a new user. Requires username and password in the request body.
POST /login: Authenticate a user. Requires username and password in the request body.
POST /blind_signature: Generate a blind signature. Requires message in the request body.
POST /receive_block: Receive a block in the blockchain. Requires public_key, blind_signature, and message in the request body.


Testing

To run the tests, use the following command: python -m unittest discover -v

