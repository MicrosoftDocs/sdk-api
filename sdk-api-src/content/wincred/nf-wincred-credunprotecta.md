---
UID: NF:wincred.CredUnprotectA
title: CredUnprotectA function
author: windows-sdk-content
description: Decrypts credentials that were previously encrypted by using the CredProtect function.
old-location: security\credunprotect.htm
tech.root: secauthn
ms.assetid: 7a22fb2b-edfc-45f2-b2d2-729f3761584d
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: CredUnprotect, CredUnprotect function [Security], CredUnprotectA, CredUnprotectW, security.credunprotect, wincred/CredUnprotect, wincred/CredUnprotectA, wincred/CredUnprotectW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredUnprotectW (Unicode) and CredUnprotectA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Security-credentials-l1-1-0.dll
api_name:
 - CredUnprotect
 - CredUnprotectA
 - CredUnprotectW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CredUnprotectA function


## -description


The <b>CredUnprotect</b> function decrypts credentials that were previously encrypted by using the <a href="https://msdn.microsoft.com/1e299dfb-2ffe-463c-9e2c-b7774a2216e3">CredProtect</a> function. The credentials must have been encrypted in the same security context in which <b>CredUnprotect</b> is called.


## -parameters




### -param fAsSelf [in]

Set to <b>TRUE</b> to specify that the credentials were encrypted in the security context of the current process. Set to <b>FALSE</b> to specify that credentials were encrypted in the security context of the calling thread security context.


### -param pszProtectedCredentials [in]

A pointer to a string that specifies the encrypted credentials.


### -param cchProtectedCredentials [in]

The size, in characters, of the <i>pszProtectedCredentials</i> buffer.


### -param pszCredentials [out]

A pointer to a string that, on output, receives the decrypted credentials.


### -param pcchMaxChars [in, out]

The size, in characters of the <i>pszCredentials</i> buffer. On output, if the <i>pszCredentials</i> is not of sufficient size to receive the encrypted credentials, this parameter specifies the required size, in characters, of the <i>pszCredentials</i> buffer.


## -returns



<b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>.

For extended error information, call the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. The following table shows common values for the <b>GetLastError</b> function.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>ERROR_NOT_CAPABLE</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The security context used to encrypt the credentials is different from the security context used to decrypt the credentials.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>ERROR_INSUFFICIENT_BUFFER</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The <i>pszCredentials</i> buffer was of insufficient size.

</td>
</tr>
</table>
 



