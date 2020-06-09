---
UID: NN:credentialprovider.ICredentialProviderSetUserArray
title: ICredentialProviderSetUserArray (credentialprovider.h)
description: Provides a method that enables a credential provider to receive the set of users that will be shown in the logon or credential UI.
helpviewer_keywords: ["ICredentialProviderSetUserArray","ICredentialProviderSetUserArray interface [Windows Shell]","ICredentialProviderSetUserArray interface [Windows Shell]","described","credentialprovider/ICredentialProviderSetUserArray","shell.ICredentialProviderSetUserArray"]
old-location: shell\ICredentialProviderSetUserArray.htm
tech.root: shell
ms.assetid: 85422EF5-8A8E-4e14-BD32-953C31A9D401
ms.date: 12/05/2018
ms.keywords: ICredentialProviderSetUserArray, ICredentialProviderSetUserArray interface [Windows Shell], ICredentialProviderSetUserArray interface [Windows Shell],described, credentialprovider/ICredentialProviderSetUserArray, shell.ICredentialProviderSetUserArray
f1_keywords:
- credentialprovider/ICredentialProviderSetUserArray
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
- ICredentialProviderSetUserArray
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICredentialProviderSetUserArray interface


## -description


Provides a method that enables a credential provider to receive the set of users that will be shown in the logon or credential UI.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProviderSetUserArray</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICredentialProviderSetUserArray</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICredentialProviderSetUserArray</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidersetuserarray-setuserarray">SetUserArray</a>
</td>
<td align="left" width="63%">
Called by the system during the initialization of a logon or credential UI to retrieve the set of users to show in that UI.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Implement this interface for credential providers that have a need to know which users will appear in the logon or credential UI.

<h3><a id="When_to_use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to use</h3>
This interface is used only by the Windows credential provider framework. Its method should not be called by other parties.




## -see-also






<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruserarray">ICredentialProviderUserArray</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

