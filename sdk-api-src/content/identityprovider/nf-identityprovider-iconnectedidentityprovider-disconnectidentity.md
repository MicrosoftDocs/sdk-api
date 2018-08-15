---
UID: NF:identityprovider.IConnectedIdentityProvider.DisconnectIdentity
title: IConnectedIdentityProvider::DisconnectIdentity
author: windows-sdk-content
description: Disconnects an online identity from the current domain user.
old-location: security\iconnectedidentityprovider_disconnectidentity.htm
old-project: secauthn
ms.assetid: D7869001-5412-48C9-9C31-0181A9366965
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DisconnectIdentity, DisconnectIdentity method [Security], DisconnectIdentity method [Security],IConnectedIdentityProvider interface, IConnectedIdentityProvider interface [Security],DisconnectIdentity method, IConnectedIdentityProvider.DisconnectIdentity, IConnectedIdentityProvider::DisconnectIdentity, identityprovider/IConnectedIdentityProvider::DisconnectIdentity, security.iconnectedidentityprovider_disconnectidentity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: identityprovider.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: IDENTITY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Identityprovider.h
api_name:
 - IConnectedIdentityProvider.DisconnectIdentity
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IConnectedIdentityProvider::DisconnectIdentity


## -description


Disconnects an online identity from the current domain user.


## -parameters






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




<a href="https://msdn.microsoft.com/0AF5036B-326E-4FBE-9F26-18F532EF0BB3">IConnectedIdentityProvider</a>
 

 

