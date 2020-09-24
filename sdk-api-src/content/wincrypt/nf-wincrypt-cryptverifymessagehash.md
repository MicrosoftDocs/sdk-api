---
UID: NF:wincrypt.CryptVerifyMessageHash
title: CryptVerifyMessageHash function (wincrypt.h)
description: The CryptVerifyMessageHash function verifies the hash of specified content.
helpviewer_keywords: ["CryptVerifyMessageHash","CryptVerifyMessageHash function [Security]","_crypto2_cryptverifymessagehash","security.cryptverifymessagehash","wincrypt/CryptVerifyMessageHash"]
old-location: security\cryptverifymessagehash.htm
tech.root: security
ms.assetid: 3b5185b9-e24b-4302-a60c-74ccbd19077c
ms.date: 12/05/2018
ms.keywords: CryptVerifyMessageHash, CryptVerifyMessageHash function [Security], _crypto2_cryptverifymessagehash, security.cryptverifymessagehash, wincrypt/CryptVerifyMessageHash
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
 - CryptVerifyMessageHash
 - wincrypt/CryptVerifyMessageHash
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
 - CryptVerifyMessageHash
---

# CryptVerifyMessageHash function


## -description

The <b>CryptVerifyMessageHash</b> function verifies the <a href="/windows/desktop/SecGloss/h-gly">hash</a> of specified content.

## -parameters

### -param pHashPara [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_hash_message_para">CRYPT_HASH_MESSAGE_PARA</a> structure containing hash parameters.

### -param pbHashedBlob [in]

A pointer to a buffer containing original content and its hash.

### -param cbHashedBlob [in]

The size, in bytes, of the original hash buffer.

### -param pbToBeHashed [out]

A pointer to a buffer to receive the original content that was hashed. 




This parameter can be <b>NULL</b> if the original content is not needed for additional processing, or to set the size of the original content for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbToBeHashed [in, out]

A pointer to a <b>DWORD</b> specifying the size, in bytes, of the <i>pbToBeHashed</i> buffer. When the function returns, this variable contains the size, in bytes, of the original content copied to <i>pbToBeHashed</i>. The original content will not be returned if this parameter is <b>NULL</b>. 




<div class="alert"><b>Note</b>  When processing the data returned, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

### -param pbComputedHash [out, optional]

A pointer to a buffer to receive the computed hash. This parameter can be <b>NULL</b> if the created hash is not needed for additional processing, or to set the size of the original content for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbComputedHash [in, out, optional]

A pointer to a <b>DWORD</b> specifying the size, in bytes, of the <i>pbComputedHash</i> buffer. When the function returns, this variable contains the size, in bytes, of the created hash. The hash is not returned if this parameter is <b>NULL</b>. 




<div class="alert"><b>Note</b>  When processing the data returned, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
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
If the buffer specified by the <i>pbToBeHashed</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code, and stores the required buffer size, in bytes, into the variable pointed to by <i>pcbToBeHashed</i>.

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

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifydetachedmessagehash">CryptVerifyDetachedMessageHash</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>