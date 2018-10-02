---
UID: NN:identityprovider.IConnectedIdentityProvider
title: IConnectedIdentityProvider
author: windows-sdk-content
description: Provides methods of interaction with a connected identity provider.
old-location: security\iconnectedidentityprovider.htm
tech.root: secauthn
ms.assetid: 0AF5036B-326E-4FBE-9F26-18F532EF0BB3
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: IConnectedIdentityProvider, IConnectedIdentityProvider interface [Security], IConnectedIdentityProvider interface [Security],described, identityprovider/IConnectedIdentityProvider, security.iconnectedidentityprovider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConnectedIdentityProvider interface


## -description


Provides methods of interaction with a connected identity provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConnectedIdentityProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IConnectedIdentityProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/945CBE34-E364-41FF-8CE4-0FB0BEF3BC69">ConnectIdentity</a>
</td>
<td align="left" width="63%">
Connects an identity to a domain user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D7869001-5412-48C9-9C31-0181A9366965">DisconnectIdentity</a>
</td>
<td align="left" width="63%">
Disconnects an online identity from the current domain user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/623A9AE8-D838-4F00-B81E-35031ADB67F5">GetUrl</a>
</td>
<td align="left" width="63%">
Returns the URL string for the specified wizard or webpage.

</td>
</tr>
</table> 

