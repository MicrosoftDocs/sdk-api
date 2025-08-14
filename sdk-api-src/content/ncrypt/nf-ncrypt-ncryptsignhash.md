---
UID: NF:ncrypt.NCryptSignHash
title: NCryptSignHash function (ncrypt.h)
description: Creates a signature of a hash value. (NCryptSignHash)
helpviewer_keywords: ["BCRYPT_PAD_PKCS1","BCRYPT_PAD_PSS","NCRYPT_SILENT_FLAG","NCryptSignHash","NCryptSignHash function [Security]","ncrypt/NCryptSignHash","security.ncryptsignhash_func"]
old-location: security\ncryptsignhash_func.htm
tech.root: security
ms.assetid: 7404e37a-d7c6-49ed-b951-6081dd2b921a
ms.date: 06/25/2025
ms.keywords: BCRYPT_PAD_PKCS1, BCRYPT_PAD_PSS, NCRYPT_SILENT_FLAG, NCryptSignHash, NCryptSignHash function [Security], ncrypt/NCryptSignHash, security.ncryptsignhash_func
req.header: ncrypt.h
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
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptSignHash
 - ncrypt/NCryptSignHash
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ncrypt.dll
api_name:
 - NCryptSignHash
---

# NCryptSignHash function


## -description

The **NCryptSignHash** function creates a signature over data to be signed.

## -parameters

### -param hKey [in]

The handle of the private key to use to generate the signature.

### -param pPaddingInfo [in, optional]

A pointer to a structure that contains padding information. The actual type of structure this parameter points to depends on the value of the *dwFlags* parameter. When *dwFlags* is `0`, this parameter must be `NULL`.

### -param pbHashValue [in]

A pointer to a buffer that contains the input to be signed. The *cbHashValue* parameter contains the size of this buffer.

**Note:** The parameter name *pbHashValue* is a misnomer due to the history of this API.

For many signature algorithms (DSA, RSA, ECDSA, HashML-DSA, etc.), the signature routine is defined to take the result of a hash function as input. In these algorithms, the original message to be signed must first be hashed, and the resultant hash value (pre-hash) is passed in the *pbHashValue* buffer.

However, some signature algorithms (pure ML-DSA, pure SLH-DSA, etc.) allow direct signing of arbitrary sized data. For these algorithms the *pbHashValue* buffer contains the input to be signed. Signer and verifier must agree on how to construct this input, but there is no requirement for a pre-hash to be involved. Signing a very large buffer directly may harm interoperability.

In either case, the *pbHashValue* buffer represents the input to be signed.

### -param cbHashValue [in]

The size, in bytes, of the *pbHashValue* buffer.

### -param pbSignature [out]

The address of a buffer to receive the signature produced by this function. The *cbSignature* parameter contains the size of this buffer.

If this parameter is `NULL`, this function will calculate the size required for the signature and return the size in the location pointed to by the *pcbResult* parameter.

### -param cbSignature [in]

The size, in bytes, of the *pbSignature* buffer. This parameter is ignored if the *pbSignature* parameter is `NULL`.

### -param pcbResult [out]

A pointer to a **DWORD** variable that receives the number of bytes copied to the *pbSignature* buffer. 

If *pbSignature* is `NULL`, this receives the size, in bytes, required for the signature.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. The allowed set of flags depends on the type of key specified by the *hKey* parameter.

This can be zero or a combination of one or more of the following values:

| Value | Meaning |
|-------|---------|
| **NCRYPT_PAD_PKCS1_FLAG** | Use the RSA PKCS1 padding scheme. The *pPaddingInfo* parameter is a pointer to a [BCRYPT_PKCS1_PADDING_INFO](../bcrypt/ns-bcrypt-bcrypt_pkcs1_padding_info.md) structure. |
| **NCRYPT_PAD_PSS_FLAG** | Use the RSA Probabilistic Signature Scheme (PSS) padding scheme. The *pPaddingInfo* parameter is a pointer to a [BCRYPT_PSS_PADDING_INFO](../bcrypt/ns-bcrypt-bcrypt_pss_padding_info.md) structure. |
| **NCRYPT_PAD_PQDSA_FLAG** | Use the PQ padding scheme for ML-DSA or SLH-DSA. The *pPaddingInfo* parameter is a pointer to a [BCRYPT_PQDSA_PADDING_INFO](/windows/win32/seccng/bcrypt/ns-bcrypt-bcrypt_pqdsa_padding_info) structure.<br/><br/>**Note:** This must be set if using a pre-hash ML-DSA variant. |
| **NCRYPT_SILENT_FLAG** | Requests that the key storage provider (KSP) not display any user interface. If the provider must display the UI to operate, the call fails and the KSP should set the **NTE_SILENT_CONTEXT** error code as the last error. |

## -returns

Returns a status code that indicates the success or failure of the function.

Possible return codes include, but are not limited to, the following:

| Return code | Description |
|-------------|-------------|
| **ERROR_SUCCESS** | The function was successful. |
| **NTE_BAD_ALGID** | The key represented by the *hKey* parameter does not support signing. |
| **NTE_BAD_FLAGS** | The *dwFlags* parameter contains a value that is not valid. |
| **NTE_INVALID_HANDLE** | The *hKey* parameter is not valid. |
| **NTE_INVALID_PARAMETER** | One or more parameters are not valid. |
| **NTE_NO_MEMORY** | A memory allocation failure occurred. |

## -remarks

A service must not call this function from its [StartService Function](../winsvc/nf-winsvc-startservicea.md). If a service calls this function from its **StartService** function, a deadlock can occur, and the service may stop responding.
