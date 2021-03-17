---
UID: NF:identityprovider.IConnectedIdentityProvider.ConnectIdentity
title: IConnectedIdentityProvider::ConnectIdentity (identityprovider.h)
description: Connects an identity to a domain user.
helpviewer_keywords: ["ConnectIdentity","ConnectIdentity method [Security]","ConnectIdentity method [Security]","IConnectedIdentityProvider interface","IConnectedIdentityProvider interface [Security]","ConnectIdentity method","IConnectedIdentityProvider.ConnectIdentity","IConnectedIdentityProvider::ConnectIdentity","identityprovider/IConnectedIdentityProvider::ConnectIdentity","security.iconnectedidentityprovider_connectidentity"]
old-location: security\iconnectedidentityprovider_connectidentity.htm
tech.root: security
ms.assetid: 945CBE34-E364-41FF-8CE4-0FB0BEF3BC69
ms.date: 12/05/2018
ms.keywords: ConnectIdentity, ConnectIdentity method [Security], ConnectIdentity method [Security],IConnectedIdentityProvider interface, IConnectedIdentityProvider interface [Security],ConnectIdentity method, IConnectedIdentityProvider.ConnectIdentity, IConnectedIdentityProvider::ConnectIdentity, identityprovider/IConnectedIdentityProvider::ConnectIdentity, security.iconnectedidentityprovider_connectidentity
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
 - IConnectedIdentityProvider::ConnectIdentity
 - identityprovider/IConnectedIdentityProvider::ConnectIdentity
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
 - IConnectedIdentityProvider.ConnectIdentity
---

# IConnectedIdentityProvider::ConnectIdentity


## -description

Connects an identity to a domain user.

## -parameters

### -param AuthBuffer [in]

A marshaled authentication buffer <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure that contains the credential of the online identity. The buffer can be constructed by the caller by using the <a href="/windows/desktop/api/wincred/nf-wincred-credpackauthenticationbuffera">CredPackAuthenticationBuffer</a> function with the CRED_PACK_ID_PROVIDER_CREDENTIALS option or returned by an online identity credential provider from the <a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforwindowscredentialsa">CredUIPromptForWindowsCredentials</a> function. The buffer can be optionally encrypted by calling the <a href="/windows/desktop/api/sspi/nf-sspi-sspiencryptauthidentityex">SspiEncryptAuthIdentityEx</a> function with the SEC_WINNT_AUTH_IDENTITY_ENCRYPT_SAME_LOGON option.

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

<a href="/windows/desktop/api/identityprovider/nn-identityprovider-iconnectedidentityprovider">IConnectedIdentityProvider</a>