---
UID: NF:wincrypt.CryptVerifyDetachedMessageHash
title: CryptVerifyDetachedMessageHash function (wincrypt.h)
description: The CryptVerifyDetachedMessageHash function verifies a detached hash.
helpviewer_keywords: ["CryptVerifyDetachedMessageHash","CryptVerifyDetachedMessageHash function [Security]","_crypto2_cryptverifydetachedmessagehash","security.cryptverifydetachedmessagehash","wincrypt/CryptVerifyDetachedMessageHash"]
old-location: security\cryptverifydetachedmessagehash.htm
tech.root: security
ms.assetid: b529b9e2-9798-4548-a44f-c330524a3e6b
ms.date: 12/05/2018
ms.keywords: CryptVerifyDetachedMessageHash, CryptVerifyDetachedMessageHash function [Security], _crypto2_cryptverifydetachedmessagehash, security.cryptverifydetachedmessagehash, wincrypt/CryptVerifyDetachedMessageHash
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptVerifyDetachedMessageHash
 - wincrypt/CryptVerifyDetachedMessageHash
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptVerifyDetachedMessageHash
---

# CryptVerifyDetachedMessageHash function


## -description

The <b>CryptVerifyDetachedMessageHash</b> function verifies a detached <a href="/windows/desktop/SecGloss/h-gly">hash</a>.

## -parameters

### -param pHashPara [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_hash_message_para">CRYPT_HASH_MESSAGE_PARA</a> structure containing the hash parameters.

### -param pbDetachedHashBlob [in]

A pointer to the encoded, detached hash.

### -param cbDetachedHashBlob [in]

The size, in bytes, of the detached hash.

### -param cToBeHashed [in]

Number of elements in the <i>rgpbToBeHashed</i> and <i>rgcbToBeHashed</i> arrays.

### -param rgpbToBeHashed [in]

Array of pointers to content buffers to be hashed.

### -param rgcbToBeHashed [in]

Array of sizes, in bytes, for the content buffers pointed to by the elements of the <i>rgcbToBeHashed</i> array.

### -param pbComputedHash [out]

A pointer to a buffer to receive the computed hash. 




This parameter can be <b>NULL</b> if the newly created hash is not needed for additional processing, or to set the size of the hash for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbComputedHash [in, out]

A pointer to a <b>DWORD</b> specifying the size, in bytes, of the <i>pbComputedHash</i> buffer. When the function returns, this <b>DWORD</b> contains the size, in bytes, of the created hash. The hash will not be returned if this parameter is <b>NULL</b>. 




<div class="alert"><b>Note</b>  When processing the data returned , applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE).

For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following lists the error codes most commonly returned by the 
		       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNEXPECTED_MSG_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Not a hashed cryptographic message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/SecGloss/m-gly">message encoding type</a> is not valid. Currently only PKCS_7_ASN_ENCODING is supported. The <b>cbSize</b> in *<i>pHashPara</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pbComputedHash</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code, and stores the required buffer size, in bytes, into the variable pointed to by <i>pcbComputedHash</i>.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a>, and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgethashparam">CryptGetHashParam</a> might be propagated to this function. <p class="note">If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>. 

</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifymessagehash">CryptVerifyMessageHash</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>