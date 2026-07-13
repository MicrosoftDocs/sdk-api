---
UID: NF:bcrypt.BCryptGenerateKeyPair
title: BCryptGenerateKeyPair function (bcrypt.h)
description: Creates an empty public/private key pair.
helpviewer_keywords: ["BCRYPT_DH_ALGORITHM","BCRYPT_DSA_ALGORITHM","BCRYPT_ECDH_P256_ALGORITHM","BCRYPT_ECDH_P384_ALGORITHM","BCRYPT_ECDH_P521_ALGORITHM","BCRYPT_ECDSA_P256_ALGORITHM","BCRYPT_ECDSA_P384_ALGORITHM","BCRYPT_ECDSA_P521_ALGORITHM","BCRYPT_RSA_ALGORITHM","BCryptGenerateKeyPair","BCryptGenerateKeyPair function [Security]","bcrypt/BCryptGenerateKeyPair","security.bcryptgeneratekeypair_func"]
old-location: security\bcryptgeneratekeypair_func.htm
tech.root: security
ms.assetid: cdf0de2e-2445-45e3-91ba-89791a0c0642
ms.date: 06/16/2025
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

The **BCryptGenerateKeyPair** function creates an empty public/private key pair. After you create a key by using this function, you can use the [BCryptSetProperty](nf-bcrypt-bcryptsetproperty.md) function to set its properties; however, the key cannot be used until the [BCryptFinalizeKeyPair](nf-bcrypt-bcryptfinalizekeypair.md) function is called.

## -parameters

### -param hAlgorithm [in, out]

The handle of an algorithm provider that uses asymmetric key pairs. Examples of types of algorithms include Signing, Asymmetric encryption, Key agreement, and Key encapsulation mechanism. This handle is obtained by calling the [BCryptOpenAlgorithmProvider](nf-bcrypt-bcryptopenalgorithmprovider.md) function, or may be a [CNG Algorithm Pseudo-handle](/windows/win32/seccng/cng-algorithm-pseudo-handles).

### -param phKey [out]

A pointer to a **BCRYPT_KEY_HANDLE** that receives the handle of the key. This handle is used in subsequent functions that require a key, such as [BCryptEncrypt](nf-bcrypt-bcryptencrypt.md). This handle must be released when it is no longer needed by passing it to the [BCryptDestroyKey](nf-bcrypt-bcryptdestroykey.md) function.

### -param dwLength [in]

The length, in bits, of the key. Algorithm providers have different key size restrictions for each standard asymmetric algorithm.

| Algorithm identifier | Meaning |
|--|--|
| **BCRYPT_DH_ALGORITHM** | The key size must be greater than or equal to 512 bits, less than or equal to 4096 bits, and must be a multiple of 64. |
| **BCRYPT_DSA_ALGORITHM** | Prior to Windows 8, the key size must be greater than or equal to 512 bits, less than or equal to 1024 bits, and must be a multiple of 64.<br/><br/>Beginning with Windows 8, the key size must be greater than or equal to 512 bits, less than or equal to 3072 bits, and must be a multiple of 64. Processing for key sizes less than or equal to 1024 bits adheres to FIPS 186-2. Processing for key sizes greater than 1024 and less than or equal to 3072 adheres to FIPS 186-3. |
| **BCRYPT_ECDH_P256_ALGORITHM** | The key size must be 256 bits. |
| **BCRYPT_ECDH_P384_ALGORITHM** | The key size must be 384 bits. |
| **BCRYPT_ECDH_P521_ALGORITHM** | The key size must be 521 bits. |
| **BCRYPT_ECDSA_P256_ALGORITHM** | The key size must be 256 bits. |
| **BCRYPT_ECDSA_P384_ALGORITHM** | The key size must be 384 bits. |
| **BCRYPT_ECDSA_P521_ALGORITHM** | The key size must be 521 bits. |
| **BCRYPT_MLDSA_ALGORITHM** | The key size must be 0.<br/><br/>For ML-DSA use [BCryptSetProperty](nf-bcrypt-bcryptsetproperty.md) with **BCRYPT_PARAMETER_SET_NAME** to specify the parameter set for the key. This must be done before finalizing the key with [BCryptFinalizeKeyPair](nf-bcrypt-bcryptfinalizekeypair.md).<br/><br/>**Windows Insiders (build 27843):** Support for ML-DSA begins. |
| **BCRYPT_MLKEM_ALGORITHM** | The key size must be 0.<br/><br/>For ML-KEM use [BCryptSetProperty](nf-bcrypt-bcryptsetproperty.md) with **BCRYPT_PARAMETER_SET_NAME** to specify the parameter set tfor the key. This must be done before finalizing the key with [BCryptFinalizeKeyPair](nf-bcrypt-bcryptfinalizekeypair.md).<br/><br/>**Windows Insiders (build 27843):** Support for ML-KEM begins. |
| **BCRYPT_RSA_ALGORITHM** | The key size must be greater than or equal to 512 bits, less than or equal to 16384 bits, and must be a multiple of 64. |

### -param dwFlags [in]

A set of flags that modify the behavior of this function. The allowed set of flags depends on the algorithm specified by the *hAlgorithm* parameter.

This can be zero or the following value:

| Value | Meaning |
|-------|---------|
| **BCRYPT_NO_KEY_VALIDATION** | Opt out of any applicable FIPS self-tests on key generation.<br/><br/>**Note:** Only currently supported for ML-KEM<br/><br/>**Windows Insiders (build 27843):** Support for ML-KEM begins. |

## -returns

Returns a status code that indicates the success or failure of the function.

Possible return codes include, but are not limited to, the following:

| Return code | Description |
|--|--|
| **STATUS_SUCCESS** | The function was successful. |
| **STATUS_INVALID_HANDLE** | The algorithm handle in the *hAlgorithm* parameter is not valid. |
| **STATUS_INVALID_PARAMETER** | One or more parameters are not valid. |
| **STATUS_NOT_SUPPORTED** | The specified algorithm does not use asymmetric key pairs. |

## -remarks

When using a supported algorithm provider, **BCryptGenerateKeyPair** can be called either from user mode or kernel mode. Kernel mode callers can execute either at **PASSIVE_LEVEL** [IRQL](/windows/win32/SecGloss/i-gly) or **DISPATCH_LEVEL** IRQL. If the current IRQL level is **DISPATCH_LEVEL**, the handle provided in the *hAlgorithm* parameter must have been opened by using the **BCRYPT_PROV_DISPATCH** flag, and any pointers passed to the **BCryptGenerateKeyPair** function must refer to nonpaged (or locked) memory.

The caller should release *phKey* with [BCryptDestroyKey](nf-bcrypt-bcryptdestroykey.md) when the key is no longer in use.

To call this function in kernel mode, use `Cng.lib`, which is part of the Driver Development Kit (DDK). **Windows Server 2008 and Windows Vista:** To call this function in kernel mode, use `Ksecdd.lib`.

## -see-also

[BCryptDestroyKey](nf-bcrypt-bcryptdestroykey.md)
