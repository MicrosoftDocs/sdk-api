---
UID: NF:identityprovider.IConnectedIdentityProvider.DisconnectIdentity
title: IConnectedIdentityProvider::DisconnectIdentity (identityprovider.h)
description: Disconnects an online identity from the current domain user.
helpviewer_keywords: ["DisconnectIdentity","DisconnectIdentity method [Security]","DisconnectIdentity method [Security]","IConnectedIdentityProvider interface","IConnectedIdentityProvider interface [Security]","DisconnectIdentity method","IConnectedIdentityProvider.DisconnectIdentity","IConnectedIdentityProvider::DisconnectIdentity","identityprovider/IConnectedIdentityProvider::DisconnectIdentity","security.iconnectedidentityprovider_disconnectidentity"]
old-location: security\iconnectedidentityprovider_disconnectidentity.htm
tech.root: security
ms.assetid: D7869001-5412-48C9-9C31-0181A9366965
ms.date: 12/05/2018
ms.keywords: DisconnectIdentity, DisconnectIdentity method [Security], DisconnectIdentity method [Security],IConnectedIdentityProvider interface, IConnectedIdentityProvider interface [Security],DisconnectIdentity method, IConnectedIdentityProvider.DisconnectIdentity, IConnectedIdentityProvider::DisconnectIdentity, identityprovider/IConnectedIdentityProvider::DisconnectIdentity, security.iconnectedidentityprovider_disconnectidentity
req.header: identityprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Identityprovider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConnectedIdentityProvider::DisconnectIdentity
 - identityprovider/IConnectedIdentityProvider::DisconnectIdentity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Identityprovider.h
api_name:
 - IConnectedIdentityProvider.DisconnectIdentity
---

# IConnectedIdentityProvider::DisconnectIdentity


## -description

Disconnects an online identity from the current domain user.



## -returns

If the method succeeds, the method returns S_OK.

If the method fails, the method returns a Win32 error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_USER</b></dt>
</dl>
</td>
<td width="60%">
The domain user is not connected to an online identity.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/identityprovider/nn-identityprovider-iconnectedidentityprovider">IConnectedIdentityProvider</a>
