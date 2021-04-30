---
UID: NF:bcrypt.BCryptDeriveKeyCapi
title: BCryptDeriveKeyCapi function (bcrypt.h)
description: Derives a key from a hash value.
helpviewer_keywords: ["BCryptDeriveKeyCapi","BCryptDeriveKeyCapi function [Security]","bcrypt/BCryptDeriveKeyCapi","security.bcryptderivekeycapi"]
old-location: security\bcryptderivekeycapi.htm
tech.root: security
ms.assetid: bebb0767-8c54-48b7-864c-f53caea7120d
ms.date: 12/05/2018
ms.keywords: BCryptDeriveKeyCapi, BCryptDeriveKeyCapi function [Security], bcrypt/BCryptDeriveKeyCapi, security.bcryptderivekeycapi
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
 - BCryptDeriveKeyCapi
 - bcrypt/BCryptDeriveKeyCapi
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
 - BCryptDeriveKeyCapi
---

# BCryptDeriveKeyCapi function


## -description

The <b>BCryptDeriveKeyCapi</b> function derives a key from a hash value.

This function is  provided as a helper function to assist in migrating legacy Cryptography API (CAPI)–based applications to use Cryptography API: Next Generation (CNG).  The <b>BCryptDeriveKeyCapi</b> function performs the key derivation in a manner that is compatible with the CAPI <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptderivekey">CryptDeriveKey</a> function.

## -parameters

### -param hHash [in]

The handle of the hash object. The handle is obtained by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptcreatehash">BCryptCreateHash</a> function. When you have finished using the handle, you must free it by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroyhash">BCryptDestroyHash</a> function.

### -param hTargetAlg [in, optional]

The handle of the algorithm object.  This can be an <a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a> value that is compatible with the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptderivekey">CryptDeriveKey</a> function.

<div class="alert"><b>Note</b>  Limitations in CAPI and key expansion prevent the use of any hash algorithm that generates an output that is larger than 512 bits.</div>
<div> </div>

### -param pbDerivedKey [out]

A pointer to the buffer that receives the derived key.

### -param cbDerivedKey [in]

The size, in characters, of the derived key pointed to by the <i>pbDerivedKey</i> parameter.

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
The handle in the <i>hHash</i> or  <i>hTargetAlg</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value in  the <i>cbDerivedKey</i> parameter is larger than twice the output size of the hash function.

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

## -remarks

This function does not support the PK salt functionality of the CAPI <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptderivekey">CryptDeriveKey</a> function.