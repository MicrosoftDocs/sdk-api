---
UID: NF:bcrypt.BCryptDeriveKeyPBKDF2
title: BCryptDeriveKeyPBKDF2 function (bcrypt.h)
description: Derives a key from a hash value by using the PBKDF2 key derivation algorithm as defined by RFC 2898.
helpviewer_keywords: ["BCryptDeriveKeyPBKDF2","BCryptDeriveKeyPBKDF2 function [Security]","bcrypt/BCryptDeriveKeyPBKDF2","security.bcryptderivekeypbkdf2"]
old-location: security\bcryptderivekeypbkdf2.htm
tech.root: security
ms.assetid: afdddfec-a3a5-410c-998b-9a5af8e051b6
ms.date: 12/05/2018
ms.keywords: BCryptDeriveKeyPBKDF2, BCryptDeriveKeyPBKDF2 function [Security], bcrypt/BCryptDeriveKeyPBKDF2, security.bcryptderivekeypbkdf2
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCryptDeriveKeyPBKDF2
 - bcrypt/BCryptDeriveKeyPBKDF2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
api_name:
 - BCryptDeriveKeyPBKDF2
---

# BCryptDeriveKeyPBKDF2 function


## -description

The <b>BCryptDeriveKeyPBKDF2</b> function derives a key from a <a href="/windows/desktop/SecGloss/h-gly">hash</a> value by using the PBKDF2 key derivation algorithm as defined by <a href="https://www.ietf.org/rfc/rfc2898.txt">RFC 2898</a>.

## -parameters

### -param hPrf [in]

The handle of an algorithm provider that provides the pseudo-random function. This should be an algorithm provider that performs a <a href="/windows/desktop/SecGloss/m-gly">Message Authentication Code</a> computation. When you use the default Microsoft algorithm provider, any <a href="/windows/desktop/SecGloss/h-gly">hashing algorithm</a> opened by using the  <b>BCRYPT_ALG_HANDLE_HMAC_FLAG</b> flag can be used.

<div class="alert"><b>Note</b>  Only algorithms that implement the BCRYPT_IS_KEYED_HASH  property can be used to populate this parameter.</div>
<div> </div>

### -param pbPassword [in, optional]

A pointer to a buffer that contains the password parameter for the PBKDF2 key derivation algorithm. <div class="alert"><b>Note</b>  Any secret information used in the key derivation should be passed in this buffer.</div>
<div> </div>

### -param cbPassword [in]

The length, in bytes, of the data in the buffer pointed to by the <i>pbPassword</i> parameter.

### -param pbSalt [in, optional]

A pointer to a buffer that contains the salt argument  for the PBKDF2 key derivation algorithm.

<div class="alert"><b>Note</b>  Any information that is not secret and that is used in the key derivation should be passed in this buffer.</div>
<div> </div>

### -param cbSalt [in]

The length, in bytes, of the salt argument pointed to by the <i>pbSalt</i> parameter.

### -param cIterations [in]

The iteration count for the PBKDF2 key derivation algorithm.

### -param pbDerivedKey [out]

A pointer to a buffer that receives the derived key.

### -param cbDerivedKey [in]

The length, in bytes, of the derived key returned in the buffer pointed to by the <i>pbDerivedKey</i> parameter.

### -param dwFlags [in]

This parameter is reserved and must be set to zero.

## -returns

Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle in the <i>hPrf</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.
 

</td>
</tr>
</table>