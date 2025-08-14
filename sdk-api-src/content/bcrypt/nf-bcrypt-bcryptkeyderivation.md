---
UID: NF:bcrypt.BCryptKeyDerivation
title: BCryptKeyDerivation function (bcrypt.h)
description: Derives a key without requiring a secret agreement.
helpviewer_keywords: ["BCryptKeyDerivation","BCryptKeyDerivation function [Security]","bcrypt/BCryptKeyDerivation","security.bcryptkeyderivation"]
old-location: security\bcryptkeyderivation.htm
tech.root: security
ms.assetid: D0B91FFE-2E72-4AE3-A84F-DC598C02CF53
ms.date: 06/27/2025
ms.keywords: BCryptKeyDerivation, BCryptKeyDerivation function [Security], bcrypt/BCryptKeyDerivation, security.bcryptkeyderivation
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - BCryptKeyDerivation
 - bcrypt/BCryptKeyDerivation
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
 - BCryptKeyDerivation
---

# BCryptKeyDerivation function


## -description

The **BCryptKeyDerivation** function derives a key by invoking a Key Derivation Function (KDF), with all parameters explicitly being provided.

It is similar in functionality to [BCryptDeriveKey](nf-bcrypt-bcryptderivekey.md) but directly invokes a KDF algorithm, so does not require a **BCRYPT_SECRET_HANDLE** value as input.

## -parameters

### -param hKey [in]

Handle of the key derivation function (KDF) key. See Remarks.

### -param pParameterList [in, optional]

The address of a [BCryptBufferDesc](ns-bcrypt-bcryptbufferdesc.md) structure that contains the KDF parameters. This parameter is optional and can be `NULL` if it is not needed.

The parameters can be specific to a key derivation function (KDF) or generic. The following table shows the required and optional parameters for specific KDFs implemented by the Microsoft Primitive provider. Some additional information can be found in the documentation for [BCryptBuffer](ns-bcrypt-bcryptbuffer.md).

| KDF | Parameter | Required | Default |
| --- | --------- | -------- | ------- |
| SP800-108 HMAC in counter mode | KDF_LABEL          | yes | |
|                                | KDF_CONTEXT        | yes | |
|                                | KDF_HASH_ALGORITHM | yes | |
| SP800-56A  | KDF_ALGORITHMID     | yes | |
|            | KDF_PARTYUINFO      | yes | |
|            | KDF_PARTYVINFO      | yes | |
|            | KDF_HASH_ALGORITHM  | yes | |
|            | KDF_SUPPPUBINFO     | no  | "" |
|            | KDF_SUPPPRIVINFO    | no  | "" |
| PBKDF2     | KDF_HASH_ALGORITHM  | yes | |
|            | KDF_SALT            | yes | |
|            | KDF_ITERATION_COUNT | no  | 10000 |
| CAPI_KDF   | KDF_HASH_ALGORITHM  | yes | |
| TLS1_1_PRF | KDF_TLS_PRF_LABEL   | yes | |
|            | KDF_TLS_PRF_SEED    | yes | |
| TLS1_2_PRF | KDF_TLS_PRF_LABEL   | yes | |
|            | KDF_TLS_PRF_SEED    | yes | |
|            | KDF_HASH_ALGORITHM  | yes | |
| HKDF       | KDF_HKDF_INFO       | no  | "" |


For some algorithms, the **KDF_GENERIC_PARAMETER** can be used instead of specifying several parameters. This maps to KDF specific parameters in the following manner:

SP800-108 HMAC in counter mode:
 - KDF_GENERIC_PARAMETER = KDF_LABEL || 0x00 || KDF_CONTEXT

SP800-56A:
 - KDF_GENERIC_PARAMETER = KDF_ALGORITHMID || KDF_PARTYUINFO || KDF_PARTYVINFO {|| KDF_SUPPPUBINFO } {|| KDF_SUPPPRIVINFO }

PBKDF2:
 - KDF_GENERIC_PARAMETER = KDF_SALT

### -param pbDerivedKey [out]

Address of a buffer that receives the key. The *cbDerivedKey* parameter contains the size of this buffer.

### -param cbDerivedKey [in]

Size, in bytes, of the buffer pointed to by the *pbDerivedKey* parameter.

### -param pcbResult [out]

Pointer to a **ULONG** that receives the number of bytes that were copied to the buffer pointed to by the *pbDerivedKey* parameter.

### -param dwFlags [in]

Flags that modify the behavior of this function. The following value can be used with the Microsoft Primitive provider.

| Value | Meaning |
| ----- | ------- |
| **BCRYPT_CAPI_AES_FLAG** | Specifies that the target algorithm is AES and that the key therefore must be double expanded. This flag is only valid with the CAPI_KDF algorithm. |

## -returns

Returns a status code that indicates the success or failure of the function.

## -remarks

The flow for using *BCryptKeyDerivation* is to:
 1) Determine the KDF algorithm you are going to use and get a algorithm handle for it. You can use the following algorithm identifiers in the [BCryptOpenAlgorithmProvider](nf-bcrypt-bcryptopenalgorithmprovider.md):
 - BCRYPT_CAPI_KDF_ALGORITHM
 - BCRYPT_SP800108_CTR_HMAC_ALGORITHM
 - BCRYPT_SP80056A_CONCAT_ALGORITHM
 - BCRYPT_PBKDF2_ALGORITHM
 - BCRYPT_TLS1_1_KDF_ALGORITHM
 - BCRYPT_TLS1_2_KDF_ALGORITHM
 - BCRYPT_HKDF_ALGORITHM

 2) Determine the secret data from which you are going to derive a key, and supply it to [BCryptGenerateSymmetricKey](nf-bcrypt-bcryptgeneratesymmetrickey.md) with the algorithm handle, to produce a KDF key handle.

 3) Call *BCryptKeyDerivation* with the KDF key handle.

To call this function in kernel mode, use `Cng.lib`, which is part of the Driver Development Kit (DDK).
**Windows Server 2008 and Windows Vista:** To call this function in kernel mode, use Ksecdd.lib.

### HKDF

In HKDF, a distinction is made between deriving a key from either:
1) The output of a secret agreement function, which is not uniformly random, and is considered to be input keying material (IKM).
2) A uniformly random secret value.

##### The first step is to "Extract" a pseudorandom key (PRK) from the provided secret data.

This step is performed by calling [BCryptSetProperty](./nf-bcrypt-bcryptsetproperty.md) on the KDF key handle with **BCRYPT_HKDF_HASH_ALGORITHM** to set the hash algorithm to use in HMAC computations in HKDF.
This is followed by a second call to [BCryptSetProperty](./nf-bcrypt-bcryptsetproperty.md) with one of either:
1) If the provided secret data represents IKM, use **BCRYPT_HKDF_SALT_AND_FINALIZE** to provide the optional salt value and extract the PRK from the IKM and finalize the KDF key handle.
2) Otherwise, use **BCRYPT_HKDF_PRK_AND_FINALIZE** to directly transform the provided secret into the HKDF PRK and finalize the KDF key handle.

##### The second step is to "Expand" the PRK into an output derived key.
This step is performed by calling *BCryptKeyDerivation* on a finalized KDF key handle.

## -see-also

[BCryptDeriveKey](nf-bcrypt-bcryptderivekey.md)

[BCryptBufferDesc](ns-bcrypt-bcryptbufferdesc.md)

[BCryptBuffer](ns-bcrypt-bcryptbuffer.md)

[NCryptKeyDerivation](../ncrypt/nf-ncrypt-ncryptkeyderivation.md)
