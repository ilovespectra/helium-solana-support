# Set up DAO Governance on Realms

Solana Realms have created a slick UI that allows anyone with a Solana wallet to easily whip up a DAO for their community. Realms will mint you a governance token, create a council, and establish a great route for your community to engage with your project.

## Create a DAO

Navigate to <a href="https://app.realms.today/" target="_blank">Realms</a> within your Solana wallet browser and select `Create DAO`
<p align="center">
<img src="/walkthroughs/images/create.png" width="800">
  </p>

## Select Type 

Multisig Wallets, NFT Community DAO, or Community Token DAO:
<p align="center">
<img src="/walkthroughs/images/realms.png" width="800">
  </p>

## Customize

You will be asked for a name for your DAO, and be walked through some basic questions on structure. Easiest path is just to say 'yes' and select the recommended values.

## Create!

Swipe to complete the transaction to create your DAO

## Metadata

This part was fun. In order to update your icon and metadata, you'll need to fork the <a href="https://github.com/solana-labs/governance-ui" target="_blank">Governance UI</a>. (Or see <a href="https://github.com/ilovespectra/helium-solana-support/edit/main/walkthroughs/realms-guide.md#or" target="_blank"> #OR </a> below.)

<p align="center">
<img src="/walkthroughs/images/fork.png" width="800">
  </p>
  
Create a folder in your computer with the name of your DAO, inside that folder create a folder labeled `img`, and put your logo file inside there. It should look like this:
```
YOUR_DAO/img/yourlogo.png
```

-In your forked repo, navigate to `public/realms` and select `Add File`

-Drag and drop your DAO folder `YOUR_DAO/img/yourlogo.png` and commit!

-Navigate back to `public/realms` and scroll all the way down to `mainnet-beta.json`

-Hit `Edit`, scroll to the bottom, and copy/paste the last entry and modify<br>

<i>Be mindful to add a comma before your metadata, and deleting the comma after.</i>

It should look like this:
```
},
  {
    "symbol": "YOUR_SYMBOL",
    "displayName": "YOUR_DAO",
    "programId": "GovER5Lthms3bLBqWub97yVrMmEogzX7xNjdXpPPCVZw", // LEAVE THIS!
    "realmId": "YOUR_REALMS_ID_/_VIEW_PARAMS_/_PUBKEY",
    "website": "https://yourwebsite.com",
    "twitter": "@yourhandle",
    "ogImage": "/realms/YOUR_DAO/img/yourlogo.png" // <-last parameter has no comma
  } // <-last entry has no comma
]
```

<i>Optional Parameters:</i>
```
    "category": "your-category", // view the existing realms for ideas
    "bannerImage": "your-banner-image",
    "communityMint": "SHARE_YOUR_COMMUNITY_MINT_ADDRESS",
    "shortDescription": "describe your dao or project",
    "sortRank": 3, // idk what this means, tbh. they're all set to '3'
    "website": "https://your.website",
    "keywords": "keywords that apply to your community",
    "discord": "https://discord.gg/your-discord",
    "github": "https://github.com/your-github",
```

## Submit a PR

Click `Pull Requests` at the top of your repo and create a new PR, then head to the <a href="https://discord.gg/4sXW9xgQ23" target="_blank">Realms Discord</a>, get verified, and navigate to `#governance-ui` and let drop a screnshot of your PR to let the kind folks know to merge your request!

# OR

It looks like a lot of the metaplex data can be added through the desktop or mobile UI. If you don't have any interest forking and submitting a pull request, you can easily forego the need thanks to some simple interfacing Realms has enabled.
