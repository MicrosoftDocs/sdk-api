---
UID: NN:credentialprovider.ICredentialProviderUser
title: ICredentialProviderUser (credentialprovider.h)
description: Provides methods used to retrieve certain properties of an individual user included in a logon or credential UI.
helpviewer_keywords: ["ICredentialProviderUser","ICredentialProviderUser interface [Windows Shell]","ICredentialProviderUser interface [Windows Shell]","described","credentialprovider/ICredentialProviderUser","shell.ICredentialProviderUser"]
old-location: shell\ICredentialProviderUser.htm
tech.root: shell
ms.assetid: 8EE5FA54-E20E-4d24-AD73-2AE1F0090950
ms.date: 12/05/2018
ms.keywords: ICredentialProviderUser, ICredentialProviderUser interface [Windows Shell], ICredentialProviderUser interface [Windows Shell],described, credentialprovider/ICredentialProviderUser, shell.ICredentialProviderUser
f1_keywords:
- credentialprovider/ICredentialProviderUser
dev_langs:
- c++
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
req.lib: CredentialProvider.lib
req.dll: Authui.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Authui.dll
api_name:
- ICredentialProviderUser
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICredentialProviderUser interface


## -description


Provides methods used to retrieve certain properties of an individual user included in a logon or credential UI.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProviderUser</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICredentialProviderUser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICredentialProviderUser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruser-getproviderid">GetProviderID</a>
</td>
<td align="left" width="63%">
Retrieves the ID of the account provider for this user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruser-getsid">GetSid</a>
</td>
<td align="left" width="63%">
Retrieves the user's SID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruser-getstringvalue">GetStringValue</a>
</td>
<td align="left" width="63%">
Retrieves string properties from the <b>ICredentialProviderUser</b> object based on the input value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruser-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves a specified property value set for the user.

</td>
</tr>
</table> 


## -remarks



Windows 8 introduces the ability to group credential providers by user. The logon UI can display a set of users rather than a set of multiple credential providers for each user. Selecting a user then displays the individual credential provider options associated with that user.

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Third-parties do not implement this interface. An implementation is included with Windows.




## -see-also





<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidersetuserarray">ICredentialProviderSetUserArray</a>



<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruserarray">ICredentialProviderUserArray</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

