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

# CredUnprotectW function


## -description


The <b>CredUnprotect</b> function decrypts credentials that were previously encrypted by using the <a href="https://msdn.microsoft.com/1e299dfb-2ffe-463c-9e2c-b7774a2216e3">CredProtect</a> function. The credentials must have been encrypted in the same security context in which <b>CredUnprotect</b> is called.


## -parameters




### -param fAsSelf [in]

Set to <b>TRUE</b> to specify that the credentials were encrypted in the security context of the current process. Set to <b>FALSE</b> to specify that credentials were encrypted in the security context of the calling thread security context.


### -param pszProtectedCredentials [in]

A pointer to a string that specifies the encrypted credentials.


### -param cchProtectedCredentials

TBD


### -param pszCredentials [out]

A pointer to a string that, on output, receives the decrypted credentials.


### -param pcchMaxChars [in, out]

The size, in characters of the <i>pszCredentials</i> buffer. On output, if the <i>pszCredentials</i> is not of sufficient size to receive the encrypted credentials, this parameter specifies the required size, in characters, of the <i>pszCredentials</i> buffer.


#### - cchCredentials [in]

The size, in characters, of the <i>pszProtectedCredentials</i> buffer.


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
 



