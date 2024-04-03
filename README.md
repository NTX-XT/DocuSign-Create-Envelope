# DocuSign Create Envelope Instructions

This Xtension is currently set up for a Demo account, so you will need to update the "host" to your DocuSign production API endpoint, which should be in this format: `https://{server}.docusign.net`. You will also need to update the `authorizationUrl` and `tokenUrl` at the bottom of the Xtension to reference `https://account.docusign.com` rather than `https://account-d.docusign.com`

## To get this set up, you will first need to create an app in DocuSign.

- Log into DocuSign E-Signature Settings and navigate to **Apps and Keys**.
- Click on the **Add App and Integration Key** button.
- Give the App a name (I would make sure it includes that it is for NAC)
- Please make sure to add a Secret Key. Your app should look like this:

  ![Your app setup](https://ntxtemplatestorage.blob.core.windows.net/assets/xtenstions/Docusign%20Create%20Envelope/Picture1.png)

The Integration Key is going to be the Client ID, and the Secret Key is going to be the Client Secret. Copy both keys. The Secret Key is only available once, so if you do lose it, either create a new secret key or store it somewhere.
- Then add `https://us.nintex.oi/connection/api/Token` as a Return URI below.
  ![Alt](https://ntxtemplatestorage.blob.core.windows.net/assets/xtenstions/Docusign%20Create%20Envelope/Picture2.png)
- Remember to hit save at the bottom of this screen.
- In NAC, Navigate to the Xtensions tab and click on the "+" button to add a new Xtension. Upload the file attached and hit "Next"
- On the security screen, copy and paste the Integration Key as the Client ID and the Secret Key as the Client Secret. Ensure that the authorization and token URLs are pointing to the right location (the extra "-d" is for Demo accounts, so it should be omitted for production).

![alt](https://ntxtemplatestorage.blob.core.windows.net/assets/xtenstions/Docusign%20Create%20Envelope/Picture3.png)

- Hit Next and select an icon or upload a DocuSign icon for your action.
- Hit Publish and you are ready to go!
- An additional note for the action you must enter in the Account ID. This can be found in the Apps and Keys tab of DocuSign Settings.
  ![alt](https://ntxtemplatestorage.blob.core.windows.net/assets/xtenstions/Docusign%20Create%20Envelope/Picture4.png)
