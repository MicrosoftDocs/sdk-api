---
UID: NF:identityprovider.IConnectedIdentityProvider.ConnectIdentity
title: IConnectedIdentityProvider::ConnectIdentity
author: windows-sdk-content
description: Connects an identity to a domain user.
old-location: security\iconnectedidentityprovider_connectidentity.htm
old-project: secauthn
ms.assetid: 945CBE34-E364-41FF-8CE4-0FB0BEF3BC69
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ConnectIdentity, ConnectIdentity method [Security], ConnectIdentity method [Security],IConnectedIdentityProvider interface, IConnectedIdentityProvider interface [Security],ConnectIdentity method, IConnectedIdentityProvider.ConnectIdentity, IConnectedIdentityProvider::ConnectIdentity, identityprovider/IConnectedIdentityProvider::ConnectIdentity, security.iconnectedidentityprovider_connectidentity
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
 - IConnectedIdentityProvider.ConnectIdentity
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IConnectedIdentityProvider::ConnectIdentity


## -description


Connects an identity to a domain user.


## -parameters




### -param AuthBuffer [in]

A marshaled authentication buffer <a href="https://msdn.microsoft.com/a6083d76-1774-428c-85ca-fea817827d6a">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure that contains the credential of the online identity. The buffer can be constructed by the caller by using the <a href="https://msdn.microsoft.com/48ffdd7a-1969-4f6a-bbc7-2826e21ea052">CredPackAuthenticationBuffer</a> function with the CRED_PACK_ID_PROVIDER_CREDENTIALS option or returned by an online identity credential provider from the <a href="https://msdn.microsoft.com/946ac279-d30a-4a6c-a76d-d93597121427">CredUIPromptForWindowsCredentials</a> function. The buffer can be optionally encrypted by calling the <a href="https://msdn.microsoft.com/9290BEF8-24C9-47F0-B258-56ED7D67620B">SspiEncryptAuthIdentityEx</a> function with the SEC_WINNT_AUTH_IDENTITY_ENCRYPT_SAME_LOGON option.


### -param AuthBufferSize [in]

Size, in bytes, of the <i>AuthBuffer</i> parameter.


## -returns



If the method succeeds, returns S_OK.

If the method fails, returns a Win32 error code.

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
<dt><b>ERROR_LOGON_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The user name or password is not correct. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_USER_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The domain user is already connected or associated with an online identity from this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_ACCOUNT_NAME</b></dt>
</dl>
</td>
<td width="60%">
The format of the online user name is not valid. 

</td>
</tr>
</table>
 




## -remarks



The <i>AuthBuffer</i> parameter can be encrypted in the system context if the credential is collected on the secure desktop. In that case, the identity provider cannot decrypt the credential in the current process. To decrypt the buffer, the identity provider will need to send the credential to a process that is running in the system context.




## -see-also




<a href="https://msdn.microsoft.com/0AF5036B-326E-4FBE-9F26-18F532EF0BB3">IConnectedIdentityProvider</a>
 

 

