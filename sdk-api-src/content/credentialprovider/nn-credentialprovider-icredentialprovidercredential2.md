---
UID: NN:credentialprovider.ICredentialProviderCredential2
title: ICredentialProviderCredential2
author: windows-sdk-content
description: Extends the ICredentialProviderCredential interface by adding a method that retrieves the security identifier (SID) of a user. The credential is associated with that user and can be grouped under the user's tile.
old-location: shell\ICredentialProviderCredential2.htm
tech.root: shell
ms.assetid: C1C4BF88-3151-4a8b-A1EE-9616DCB6EA58
ms.author: windowssdkdev
ms.date: 11/02/2018
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


Extends the <a href="https://msdn.microsoft.com/en-us/library/Bb776029(v=VS.85).aspx">ICredentialProviderCredential</a> interface by adding a method that retrieves the security identifier (SID) of a user. The credential is associated with that user and can be grouped under the user's tile.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProviderCredential2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb776029(v=VS.85).aspx">ICredentialProviderCredential</a>. <b>ICredentialProviderCredential2</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Hh706913(v=VS.85).aspx">GetUserSid</a>
</td>
<td align="left" width="63%">
Retrieves the SID of the user that is associated with this credential.

</td>
</tr>
</table> 


## -remarks



This class is required for creating a V2 credential provider. V2 credential providers provide a personalized log on experience for the user. This occurs by the credential provider telling the Logon UI what sign in options are available for a user. It is recommended that new credential providers should be V2 credential providers. 

In order to create an <b>ICredentialProviderCredential2</b> instance, a valid SID needs to be returned by the <a href="https://msdn.microsoft.com/en-us/library/Hh706913(v=VS.85).aspx">GetUserSid</a> function. Valid is defined by the returned SID being for one of the users currently enumerated by the Logon UI.

A useful tool for getting the available users and determining which ones you want to associate with is the <a href="https://msdn.microsoft.com/en-us/library/Hh706923(v=VS.85).aspx">ICredentialProviderUserArray</a> object. This object contains a list of <a href="https://msdn.microsoft.com/en-us/library/Hh706922(v=VS.85).aspx">ICredentialProviderUser</a> objects that can be queried to gain information about the users that will be enumerated. For example you could gain the user's SID or username using <a href="https://msdn.microsoft.com/en-us/library/Hh706930(v=VS.85).aspx">GetStringValue</a> with a passed in parameter of <b>PKEY_Identity_PrimarySid</b> or <b>PKEY_Identity_USerName</b> respectively. You can even filter the results using <a href="https://msdn.microsoft.com/en-us/library/Hh706927(v=VS.85).aspx">SetProviderFilter</a> to only display a subset of available users.

Using the <a href="https://msdn.microsoft.com/en-us/library/Hh706923(v=VS.85).aspx">ICredentialProviderUserArray</a> is optional, but it is a convenient way to get the necessary information to make valid SID values. In order to get a list of users that will be enumerated by the Logon UI, implement the <a href="https://msdn.microsoft.com/en-us/library/Hh706920(v=VS.85).aspx">ICredentialProviderSetUserArray</a> interface to get the <b>ICredentialProviderUserArray</b> object from <a href="https://msdn.microsoft.com/en-us/library/Hh706921(v=VS.85).aspx">SetUserArray</a>. Logon UI calls <b>SetUserArray</b> before <a href="https://msdn.microsoft.com/en-us/library/Bb776039(v=VS.85).aspx">GetCredentialCount</a>, so the <b>ICredentialProviderUserArray</b> object is ready when a credential provider is about to return credentials.

A V2 credential provider  is represented by an icon displayed underneath the "Sign-in options" link. In order to provide an icon for your credential provider, define a <a href="https://msdn.microsoft.com/en-us/library/Bb762490(v=VS.85).aspx">CREDENTIAL_PROVIDER_FIELD_TYPE</a> of  <b>CPFT_TILE_IMAGE</b> in the credential itself. Then make sure the <i>guidFieldType</i> of the  <a href="https://msdn.microsoft.com/en-us/library/Bb773243(v=VS.85).aspx">CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</a> is set to <b>CPFG_CREDENTIAL_PROVIDER_LOGO</b>. The recommended size for an icon is 72 by 72 pixels.

Similar to specifying an icon for your credential provider, you can also specify a text string to identify your credential provider. This string appears in a pop-up window when a user hovers over the icon. To do this, define a <a href="https://msdn.microsoft.com/en-us/library/Bb762490(v=VS.85).aspx">CREDENTIAL_PROVIDER_FIELD_TYPE</a> of  <b>CPFT_SMALL_TEXT</b> in the credential itself. Then make sure the <i>guidFieldType</i> of the  <a href="https://msdn.microsoft.com/en-us/library/Bb773243(v=VS.85).aspx">CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</a> is set to <b>CPFG_CREDENTIAL_PROVIDER_LABEL</b>. This string should supplement the credential provider icon described above and be descriptive enough that users understand what it is. For example, the picture password provider's description is "Picture Password".

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Implement this interface to associate credential tiles with specific user tiles in the Logon UI.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=253508">Credential Provider Framework Changes in Windows 8.docx</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt158211(v=VS.85).aspx">Credential Providers in Windows 10</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776029(v=VS.85).aspx">ICredentialProviderCredential</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh706914(v=VS.85).aspx">ICredentialProviderCredentialEvents2</a>
 

 

