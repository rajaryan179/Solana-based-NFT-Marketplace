# Solana-based-NFT-Marketplace

Key Features of the Contract
#Minting an NFT:

The mint_nft function mints a new NFT with a URI for metadata storage and assigns ownership to the user who calls it.
It initializes both the mint and the associated token account for the user.
Listing an NFT:

The list_nft function allows the NFT owner to list their token for sale on the marketplace.
The listing includes the NFT mint address, the seller's address, and the price in lamports (Solana's smallest unit).
Buying an NFT:

The buy_nft function allows a buyer to purchase an NFT from the marketplace.
Upon purchase, the buyer sends the required amount of lamports to the seller, and the NFT is transferred to the buyer. Explanation of Accounts and Data Structures
MintNft: This context handles minting, setting up the mint, token account, and metadata for the NFT.

ListNft: Handles the listing process, linking the NFT with the listing account that tracks the owner, price, and NFT details.

BuyNft: Facilitates the NFT purchase, handling the transfer of lamports (funds) and the NFT token to the buyer.

NftMetadata: Stores the metadata of an NFT, including the URI and owner address.

Listing: Represents a marketplace listing, containing the NFT mint address, the owner (seller), and the price.

 Build and Deploy Instructions
To build, deploy, and interact with the contract:

Install Anchor:



cargo install --git https://github.com/coral-xyz/anchor anchor-cli --locked
Build the Program:



anchor build
Deploy the Program:


anchor deploy
Test the Program: You can use Anchor's testing framework or Solana CLI to interact with the deployed program.

 Security Considerations
Access Control: Ensure only the NFT owner can list or transfer their NFT.
Escrow Management: Handle escrow for funds securely when trading NFTs.
Audits: Perform a third-party audit to ensure no vulnerabilities exist, especially around user funds and asset ownership.
