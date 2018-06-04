---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



