---
UID: NF:bcrypt.BCryptGenerateKeyPair
title: BCryptGenerateKeyPair function (bcrypt.h)
description: Creates an empty public/private key pair.
helpviewer_keywords: ["BCRYPT_DH_ALGORITHM","BCRYPT_DSA_ALGORITHM","BCRYPT_ECDH_P256_ALGORITHM","BCRYPT_ECDH_P384_ALGORITHM","BCRYPT_ECDH_P521_ALGORITHM","BCRYPT_ECDSA_P256_ALGORITHM","BCRYPT_ECDSA_P384_ALGORITHM","BCRYPT_ECDSA_P521_ALGORITHM","BCRYPT_RSA_ALGORITHM","BCryptGenerateKeyPair","BCryptGenerateKeyPair function [Security]","bcrypt/BCryptGenerateKeyPair","security.bcryptgeneratekeypair_func"]
old-location: security\bcryptgeneratekeypair_func.htm
tech.root: security
ms.assetid: cdf0de2e-2445-45e3-91ba-89791a0c0642
ms.date: 12/05/2018
ms.keywords: BCRYPT_DH_ALGORITHM, BCRYPT_DSA_ALGORITHM, BCRYPT_ECDH_P256_ALGORITHM, BCRYPT_ECDH_P384_ALGORITHM, BCRYPT_ECDH_P521_ALGORITHM, BCRYPT_ECDSA_P256_ALGORITHM, BCRYPT_ECDSA_P384_ALGORITHM, BCRYPT_ECDSA_P521_ALGORITHM, BCRYPT_RSA_ALGORITHM, BCryptGenerateKeyPair, BCryptGenerateKeyPair function [Security], bcrypt/BCryptGenerateKeyPair, security.bcryptgeneratekeypair_func
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - BCryptGenerateKeyPair
 - bcrypt/BCryptGenerateKeyPair
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
 - Ksecdd.sys
api_name:
 - BCryptGenerateKeyPair
---

# BCryptGenerateKeyPair function


## -description

The <b>BCryptGenerateKeyPair</b> function creates an empty public/private key pair. After you create a key by using this function, you can use the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsetproperty">BCryptSetProperty</a> function to set its properties; however, the key cannot be used until the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfinalizekeypair">BCryptFinalizeKeyPair</a> function is called.

## -parameters

### -param hAlgorithm [in, out]

Handle of an algorithm provider that supports signing, asymmetric encryption, or key agreement. This handle must have been created by using the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptopenalgorithmprovider">BCryptOpenAlgorithmProvider</a> function.

### -param phKey [out]

A pointer to a <b>BCRYPT_KEY_HANDLE</b> that receives the handle of the key. This handle is used in subsequent functions that require a key, such as <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a>. This handle must be released when it is no longer needed by passing it to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroykey">BCryptDestroyKey</a> function.

### -param dwLength [in]

The length, in bits, of the key. Algorithm providers have different key size restrictions for each standard asymmetric algorithm.

<table>
<tr>
<th>Algorithm identifier</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DH_ALGORITHM"></a><a id="bcrypt_dh_algorithm"></a><dl>
<dt><b>BCRYPT_DH_ALGORITHM</b></dt>
</dl>
</td>
<td width="60%">
The key size must be greater than or equal to 512 bits, less than or equal to 4096 bits, and must be a multiple of 64.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DSA_ALGORITHM"></a><a id="bcrypt_dsa_algorithm"></a><dl>
<dt><b>BCRYPT_DSA_ALGORITHM</b></dt>
</dl>
</td>
<td width="60%">
Prior to Windows 8, the key size must be greater than or equal to 512 bits, less than or equal to 1024 bits, and must be a multiple of 64.

Beginning with Windows 8, the key size must be greater than or equal to 512 bits, less than or equal to 3072 bits, and must be a multiple of 64. Processing for key sizes less than or equal to 1024 bits adheres to FIPS 186-2. Processing for key sizes greater than 1024 and less than or equal to 3072 adheres to FIPS 186-3.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ECDH_P256_ALGORITHM"></a><a id="bcrypt_ecdh_p256_algorithm"></a><dl>
<dt><b>BCRYPT_ECDH_P256_ALGORITHM</b></dt>
</dl>
</td>
<td width="60%">
The key size must be 256 bits.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ECDH_P384_ALGORITHM"></a><a id="bcrypt_ecdh_p384_algorithm"></a><dl>
<dt><b>BCRYPT_ECDH_P384_ALGORITHM</b></dt>
</dl>
</td>
<td width="60%">
The key size must be 384 bits.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ECDH_P521_ALGORITHM"></a><a id="bcrypt_ecdh_p521_algorithm"></a><dl>
<dt><b>BCRYPT_ECDH_P521_ALGORITHM</b></dt>
</dl>
</td>
<td width="60%">
The key size must be 521 bits.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ECDSA_P256_ALGORITHM"></a><a id="bcrypt_ecdsa_p256_algorithm"></a><dl>
<dt><b>BCRYPT_ECDSA_P256_ALGORITHM</b></dt>
</dl>
</td>
<td width="60%">
The key size must be 256 bits.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ECDSA_P384_ALGORITHM"></a><a id="bcrypt_ecdsa_p384_algorithm"></a><dl>
<dt><b>BCRYPT_ECDSA_P384_ALGORITHM</b></dt>
</dl>
</td>
<td width="60%">
The key size must be 384 bits.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ECDSA_P521_ALGORITHM"></a><a id="bcrypt_ecdsa_p521_algorithm"></a><dl>
<dt><b>BCRYPT_ECDSA_P521_ALGORITHM</b></dt>
</dl>
</td>
<td width="60%">
The key size must be 521 bits.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RSA_ALGORITHM"></a><a id="bcrypt_rsa_algorithm"></a><dl>
<dt><b>BCRYPT_RSA_ALGORITHM</b></dt>
</dl>
</td>
<td width="60%">
The key size must be greater than or equal to 512 bits, less than or equal to 16384 bits, and must be a multiple of 64.

</td>
</tr>
</table>

### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are currently defined, so this parameter should be zero.

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
The algorithm handle in the <i>hAlgorithm</i> parameter is not valid.

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
<dt><b>STATUS_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The specified provider does not support asymmetric key encryption.

</td>
</tr>
</table>

## -remarks

Depending on what processor modes a provider supports, <b>BCryptGenerateKeyPair</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hAlgorithm</i> parameter must have been opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptGenerateKeyPair</b> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroykey">BCryptDestroyKey</a>