---
UID: NN:credentialprovider.ICredentialProviderCredential2
title: ICredentialProviderCredential2
author: windows-sdk-content
description: Extends the ICredentialProviderCredential interface by adding a method that retrieves the security identifier (SID) of a user. The credential is associated with that user and can be grouped under the user's tile.
old-location: shell\ICredentialProviderCredential2.htm
tech.root: shell
ms.assetid: C1C4BF88-3151-4a8b-A1EE-9616DCB6EA58
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: ICredentialProviderCredential2, ICredentialProviderCredential2 interface [Windows Shell], ICredentialProviderCredential2 interface [Windows Shell],described, credentialprovider/ICredentialProviderCredential2, shell.ICredentialProviderCredential2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CredentialProvider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CredentialProvider.h
api_name:
 - ICredentialProviderCredential2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderCredential2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a> interface by adding a method that retrieves the security identifier (SID) of a user. The credential is associated with that user and can be grouped under the user's tile.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProviderCredential2</b> interface inherits from <a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a>. <b>ICredentialProviderCredential2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICredentialProviderCredential2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8BCB9019-40C0-4026-B3C9-ECA02B9AC871">GetUserSid</a>
</td>
<td align="left" width="63%">
Retrieves the SID of the user that is associated with this credential.

</td>
</tr>
</table> 


## -remarks



This class is required for creating a V2 credential provider. V2 credential providers provide a personalized log on experience for the user. This occurs by the credential provider telling the Logon UI what sign in options are available for a user. It is recommended that new credential providers should be V2 credential providers. 

In order to create an <b>ICredentialProviderCredential2</b> instance, a valid SID needs to be returned by the <a href="https://msdn.microsoft.com/8BCB9019-40C0-4026-B3C9-ECA02B9AC871">GetUserSid</a> function. Valid is defined by the returned SID being for one of the users currently enumerated by the Logon UI.

A useful tool for getting the available users and determining which ones you want to associate with is the <a href="https://msdn.microsoft.com/50FC43C1-B148-4e42-AB38-3559BD056855">ICredentialProviderUserArray</a> object. This object contains a list of <a href="https://msdn.microsoft.com/8EE5FA54-E20E-4d24-AD73-2AE1F0090950">ICredentialProviderUser</a> objects that can be queried to gain information about the users that will be enumerated. For example you could gain the user's SID or username using <a href="https://msdn.microsoft.com/97FFD00F-6141-472c-A60C-A9A282190C9D">GetStringValue</a> with a passed in parameter of <b>PKEY_Identity_PrimarySid</b> or <b>PKEY_Identity_USerName</b> respectively. You can even filter the results using <a href="https://msdn.microsoft.com/86FC48BF-FEEA-40c4-91CA-21FFAC210CFA">SetProviderFilter</a> to only display a subset of available users.

Using the <a href="https://msdn.microsoft.com/50FC43C1-B148-4e42-AB38-3559BD056855">ICredentialProviderUserArray</a> is optional, but it is a convenient way to get the necessary information to make valid SID values. In order to get a list of users that will be enumerated by the Logon UI, implement the <a href="https://msdn.microsoft.com/85422EF5-8A8E-4e14-BD32-953C31A9D401">ICredentialProviderSetUserArray</a> interface to get the <b>ICredentialProviderUserArray</b> object from <a href="https://msdn.microsoft.com/14A9DFBD-7B44-4983-8B02-5880017B9B04">SetUserArray</a>. Logon UI calls <b>SetUserArray</b> before <a href="https://msdn.microsoft.com/7d940d46-d4c2-4ab5-8559-416d78d3579e">GetCredentialCount</a>, so the <b>ICredentialProviderUserArray</b> object is ready when a credential provider is about to return credentials.

A V2 credential provider  is represented by an icon displayed underneath the "Sign-in options" link. In order to provide an icon for your credential provider, define a <a href="https://msdn.microsoft.com/5af9f007-9588-4574-a5ce-3f01ec0b45e8">CREDENTIAL_PROVIDER_FIELD_TYPE</a> of  <b>CPFT_TILE_IMAGE</b> in the credential itself. Then make sure the <i>guidFieldType</i> of the  <a href="https://msdn.microsoft.com/8409b4b7-c601-4e85-95f9-4272feb29028">CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</a> is set to <b>CPFG_CREDENTIAL_PROVIDER_LOGO</b>. The recommended size for an icon is 72 by 72 pixels.

Similar to specifying an icon for your credential provider, you can also specify a text string to identify your credential provider. This string appears in a pop-up window when a user hovers over the icon. To do this, define a <a href="https://msdn.microsoft.com/5af9f007-9588-4574-a5ce-3f01ec0b45e8">CREDENTIAL_PROVIDER_FIELD_TYPE</a> of  <b>CPFT_SMALL_TEXT</b> in the credential itself. Then make sure the <i>guidFieldType</i> of the  <a href="https://msdn.microsoft.com/8409b4b7-c601-4e85-95f9-4272feb29028">CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</a> is set to <b>CPFG_CREDENTIAL_PROVIDER_LABEL</b>. This string should supplement the credential provider icon described above and be descriptive enough that users understand what it is. For example, the picture password provider's description is "Picture Password".

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Implement this interface to associate credential tiles with specific user tiles in the Logon UI.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=253508">Credential Provider Framework Changes in Windows 8.docx</a>



<a href="https://msdn.microsoft.com/BCF69196-D4E4-41D0-B372-5000FD50164B">Credential Providers in Windows 10</a>



<a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a>



<a href="https://msdn.microsoft.com/47290FF7-1785-4470-B3A9-F35C5028A6FE">ICredentialProviderCredentialEvents2</a>
 

 

