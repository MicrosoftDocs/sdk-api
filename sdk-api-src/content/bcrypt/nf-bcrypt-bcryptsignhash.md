---
UID: NF:bcrypt.BCryptSignHash
title: BCryptSignHash function (bcrypt.h)
description: Creates a signature of a hash value. (BCryptSignHash)
helpviewer_keywords: ["BCRYPT_PAD_PKCS1","BCRYPT_PAD_PSS","BCryptSignHash","BCryptSignHash function [Security]","bcrypt/BCryptSignHash","security.bcryptsignhash_func"]
old-location: security\bcryptsignhash_func.htm
tech.root: security
ms.assetid: f402ea9e-89ae-4ccc-9591-aa2328287c0e
ms.date: 06/16/2025
ms.keywords: BCRYPT_PAD_PKCS1, BCRYPT_PAD_PSS, BCryptSignHash, BCryptSignHash function [Security], bcrypt/BCryptSignHash, security.bcryptsignhash_func
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
 - BCryptSignHash
 - bcrypt/BCryptSignHash
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
 - BCryptSignHash
---

# BCryptSignHash function

## -description

The **BCryptSignHash** function creates a signature over data to be signed.

## -parameters

### -param hKey [in]

The handle of the private key to use to generate the signature.

### -param pPaddingInfo [in, optional]

A pointer to a structure that contains padding information. The actual type of structure this parameter points to depends on the value of the *dwFlags* parameter. When *dwFlags* is `0`, this parameter must be `NULL`.

### -param pbInput [in, optional]

A pointer to a buffer that contains the input to be signed. The *cbInput* parameter contains the size of this buffer.

For many signature algorithms (DSA, RSA, ECDSA, HashML-DSA, etc.), the signature routine is defined to take the result of a hash function as input. In these algorithms, the original message to be signed must first be hashed, and the resultant hash value (pre-hash) is passed in the *pbInput* buffer.

However, some signature algorithms (pure ML-DSA, pure SLH-DSA, etc.) allow direct signing of arbitrary sized data. For these algorithms the *pbInput* buffer contains the input to be signed. Signer and verifier must agree on how to construct this input, but there is no requirement for a pre-hash to be involved. Signing a very large buffer directly may harm interoperability.

In either case, the *pbInput* buffer represents the input to be signed.

### -param cbInput [in]

The size, in bytes, of the *pbInput* buffer.

### -param pbOutput [out, optional]

The address of a buffer to receive the signature produced by this function. The *cbOutput* parameter contains the size of this buffer.

If this parameter is `NULL`, this function will calculate the size required for the signature and return the size in the location pointed to by the *pcbResult* parameter.

### -param cbOutput [in]

The size, in bytes, of the *pbOutput* buffer. This parameter is ignored if the *pbOutput* parameter is `NULL`.

### -param pcbResult [out]

A pointer to a **ULONG** variable that receives the number of bytes copied to the *pbOutput* buffer. 

If *pbOutput* is `NULL`, this receives the size, in bytes, required for the signature.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. The allowed set of flags depends on the type of key specified by the *hKey* parameter.

This can be zero or one of the following values:

| Value | Meaning |
|-------|---------|
| **BCRYPT_PAD_PKCS1** | Use the RSA PKCS1 signature padding scheme. The *pPaddingInfo* parameter is a pointer to a [BCRYPT_PKCS1_PADDING_INFO](ns-bcrypt-bcrypt_pkcs1_padding_info.md) structure. |
| **BCRYPT_PAD_PSS** | Use the RSA Probabilistic Signature Scheme (PSS) padding scheme. The *pPaddingInfo* parameter is a pointer to a [BCRYPT_PSS_PADDING_INFO](ns-bcrypt-bcrypt_pss_padding_info.md) structure. |
| **BCRYPT_PAD_PQDSA** | Supply extra information about how to compute the Post-Quantum Digital Signature algorithms (PQDSA) signature. The *pPaddingInfo* parameter is a pointer to a [BCRYPT_PQDSA_PADDING_INFO](/windows/win32/seccng/bcrypt/ns-bcrypt-bcrypt_pqdsa_padding_info) structure.<br/><br/>**Note:** This must be set if using a pre-hash PQDSA variant.<br/><br/>**Windows Insiders (build 27843):** Support for PQDSA begins. |

## -returns

Returns a status code that indicates the success or failure of the function.

Possible return codes include, but are not limited to, the following:

| Return code | Description |
|-------------|-------------|
| **STATUS_SUCCESS** | The function was successful. |
| **STATUS_INVALID_PARAMETER** | One of the supplied parameters is invalid. |
| **STATUS_INVALID_HANDLE** | The key handle specified by the *hKey* parameter is not valid. |
| **STATUS_NO_MEMORY** | A memory allocation failure occurred. |
| **STATUS_NOT_SUPPORTED** | The algorithm provider used to create the key handle specified by the *hKey* parameter is not a signing algorithm. |
| **STATUS_BUFFER_TOO_SMALL** | The memory size specified by the *cbOutput* parameter is not large enough to hold the signature. |

## -remarks

This function performs the Signing operation of a digital signature scheme. It takes data to be signed and a private key, with additional parameters optionally specified by *dwFlags* and *pPaddingInfo*, and produces a signature which can later be verified with the corresponding public key.

To later verify that the signature is valid, call the [BCryptVerifySignature](nf-bcrypt-bcryptverifysignature.md) function with a key containing the public key corresponding to the provided private key and identical data to be verified.

When using a supported algorithm provider, **BCryptSignHash** can be called either from user mode or kernel mode. Kernel mode callers can execute either at **PASSIVE_LEVEL** [IRQL](/windows/win32/SecGloss/i-gly) or **DISPATCH_LEVEL** IRQL. If the current IRQL level is **DISPATCH_LEVEL**, the handle provided in the *hKey* parameter must be derived from an algorithm handle returned by a provider that was opened with the **BCRYPT_PROV_DISPATCH** flag, and any pointers passed to the **BCryptSignHash** function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use `Cng.lib`, which is part of the Driver Development Kit (DDK). **Windows Server 2008 and Windows Vista:** To call this function in kernel mode, use `Ksecdd.lib`.

## -see-also

[BCryptVerifySignature](nf-bcrypt-bcryptverifysignature.md)
