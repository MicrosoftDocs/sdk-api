---
UID: NF:sspi.SspiDecryptAuthIdentityEx
title: SspiDecryptAuthIdentityEx function (sspi.h)
description: Decrypts a SEC_WINNT_AUTH_IDENTITY_OPAQUE structure.
helpviewer_keywords: ["SspiDecryptAuthIdentityEx","SspiDecryptAuthIdentityEx function [Security]","security.sspidecryptauthidentityex","sspi/SspiDecryptAuthIdentityEx"]
old-location: security\sspidecryptauthidentityex.htm
tech.root: security
ms.assetid: 86598BAA-0E87-46A9-AA1A-BF04BF0CDAFA
ms.date: 12/05/2018
ms.keywords: SspiDecryptAuthIdentityEx, SspiDecryptAuthIdentityEx function [Security], security.sspidecryptauthidentityex, sspi/SspiDecryptAuthIdentityEx
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
 - SspiDecryptAuthIdentityEx
 - sspi/SspiDecryptAuthIdentityEx
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
 - SspiDecryptAuthIdentityEx
---

# SspiDecryptAuthIdentityEx function


## -description

Decrypts a <b>SEC_WINNT_AUTH_IDENTITY_OPAQUE</b> structure.

## -parameters

### -param Options [in]

Decryption options. This parameter should be the same value as the value passed to the <a href="/windows/desktop/api/sspi/nf-sspi-sspiencryptauthidentityex">SspiEncryptAuthIdentityEx</a> function, which can be one of the following values.

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

### -param EncryptedAuthData [in, out]

 This buffer is the output of the <a href="/windows/desktop/api/sspi/nf-sspi-sspiencryptauthidentityex">SspiEncryptAuthIdentityEx</a> function.

## -returns

If the function succeeds, it returns SEC_E_OK.

If the function fails, it returns a nonzero error code.