---
UID: NF:sspi.SspiEncryptAuthIdentityEx
title: SspiEncryptAuthIdentityEx function (sspi.h)
description: Encrypts a SEC_WINNT_AUTH_IDENTITY_OPAQUE structure.
helpviewer_keywords: ["SspiEncryptAuthIdentityEx","SspiEncryptAuthIdentityEx function [Security]","security.sspiencryptauthidentityex","sspi/SspiEncryptAuthIdentityEx"]
old-location: security\sspiencryptauthidentityex.htm
tech.root: security
ms.assetid: 9290BEF8-24C9-47F0-B258-56ED7D67620B
ms.date: 12/05/2018
ms.keywords: SspiEncryptAuthIdentityEx, SspiEncryptAuthIdentityEx function [Security], security.sspiencryptauthidentityex, sspi/SspiEncryptAuthIdentityEx
req.header: sspi.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SspiEncryptAuthIdentityEx
 - sspi/SspiEncryptAuthIdentityEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SspiEncryptAuthIdentityEx
---

# SspiEncryptAuthIdentityEx function


## -description

Encrypts a <b>SEC_WINNT_AUTH_IDENTITY_OPAQUE</b> structure.

## -parameters

### -param Options [in]

Encryption options. This can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>SEC_WINNT_AUTH_IDENTITY_ENCRYPT_SAME_LOGON</dt>
</dl>
</td>
<td width="60%">
The encrypted structure can only be decrypted by a security context in the same logon session. This option is used to protect an identity buffer that is being sent over a local RPC.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>SEC_WINNT_AUTH_IDENTITY_ENCRYPT_SAME_PROCESS</dt>
</dl>
</td>
<td width="60%">
The encrypted structure can only be decrypted by the same process. Calling the function with this option is equivalent to calling <a href="/windows/desktop/api/sspi/nf-sspi-sspiencryptauthidentity">SspiEncryptAuthIdentity</a>. This option is used to protect an identity buffer that is being persisted in a process's private memory for an extended period.

</td>
</tr>
</table>

### -param AuthData [in, out]

On input, a pointer to an identity buffer to encrypt. This buffer must be prepared for encryption prior to the call to this function. This can be done by calling the function <a href="/windows/desktop/api/sspi/nf-sspi-sspiencryptauthidentity">SspiEncryptAuthIdentity</a>. On output, the encrypted identity buffer.

## -returns

If the function succeeds, it returns SEC_E_OK.

If the function fails, it returns a nonzero error code.

## -remarks

To transfer credentials securely across processes, applications typically call this function with the SEC_WINNT_AUTH_IDENTITY_ENCRYPT_SAME_LOGON option,  followed by <a href="/windows/desktop/api/sspi/nf-sspi-sspimarshalauthidentity">SspiMarshalAuthIdentity</a> to obtain a marshaled authentication buffer and its length. 
For example, Online Identity Credential Provider does this to return the authentication buffer from their <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-getserialization">ICredentialProviderCredential::GetSerialization</a> method.