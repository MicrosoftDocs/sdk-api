---
UID: NN:identityprovider.IConnectedIdentityProvider
title: IConnectedIdentityProvider (identityprovider.h)
description: Provides methods of interaction with a connected identity provider.
helpviewer_keywords: ["IConnectedIdentityProvider","IConnectedIdentityProvider interface [Security]","IConnectedIdentityProvider interface [Security]","described","identityprovider/IConnectedIdentityProvider","security.iconnectedidentityprovider"]
old-location: security\iconnectedidentityprovider.htm
tech.root: security
ms.assetid: 0AF5036B-326E-4FBE-9F26-18F532EF0BB3
ms.date: 12/05/2018
ms.keywords: IConnectedIdentityProvider, IConnectedIdentityProvider interface [Security], IConnectedIdentityProvider interface [Security],described, identityprovider/IConnectedIdentityProvider, security.iconnectedidentityprovider
f1_keywords:
- identityprovider/IConnectedIdentityProvider
dev_langs:
- c++
req.header: identityprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
- Identityprovider.h
api_name:
- IConnectedIdentityProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConnectedIdentityProvider interface


## -description


Provides methods of interaction with a connected identity provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConnectedIdentityProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConnectedIdentityProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConnectedIdentityProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nf-identityprovider-iconnectedidentityprovider-connectidentity">ConnectIdentity</a>
</td>
<td align="left" width="63%">
Connects an identity to a domain user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nf-identityprovider-iconnectedidentityprovider-disconnectidentity">DisconnectIdentity</a>
</td>
<td align="left" width="63%">
Disconnects an online identity from the current domain user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nf-identityprovider-iconnectedidentityprovider-geturl">GetUrl</a>
</td>
<td align="left" width="63%">
Returns the URL string for the specified wizard or webpage.

</td>
</tr>
</table> 

