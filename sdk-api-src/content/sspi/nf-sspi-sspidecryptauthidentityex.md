---
UID: NF:sspi.SspiDecryptAuthIdentityEx
title: SspiDecryptAuthIdentityEx function
author: windows-sdk-content
description: Decrypts a SEC_WINNT_AUTH_IDENTITY_OPAQUE structure.
old-location: security\sspidecryptauthidentityex.htm
tech.root: secauthn
ms.assetid: 86598BAA-0E87-46A9-AA1A-BF04BF0CDAFA
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: SspiDecryptAuthIdentityEx, SspiDecryptAuthIdentityEx function [Security], security.sspidecryptauthidentityex, sspi/SspiDecryptAuthIdentityEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SspiDecryptAuthIdentityEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SspiDecryptAuthIdentityEx function


## -description


Decrypts a <b>SEC_WINNT_AUTH_IDENTITY_OPAQUE</b> structure. 


## -parameters




### -param Options [in]

Decryption options. This parameter should be the same value as the value passed to the <a href="https://msdn.microsoft.com/9290BEF8-24C9-47F0-B258-56ED7D67620B">SspiEncryptAuthIdentityEx</a> function, which can be one of the following values.

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
The encrypted structure can only be decrypted by the same process. Calling the function with this option is equivalent to calling <a href="https://msdn.microsoft.com/4460f7ec-35fd-4ad1-8c20-dda9f4d3477a">SspiEncryptAuthIdentity</a>. This option is used to protect an identity buffer that is being persisted in a process's private memory for an extended period.

</td>
</tr>
</table>
 


### -param EncryptedAuthData [in, out]

 This buffer is the output of the <a href="https://msdn.microsoft.com/9290BEF8-24C9-47F0-B258-56ED7D67620B">SspiEncryptAuthIdentityEx</a> function. 


## -returns



If the function succeeds, it returns SEC_E_OK.

If the function fails, it returns a nonzero error code.



