---
UID: NF:bcrypt.BCryptOpenAlgorithmProvider
title: BCryptOpenAlgorithmProvider function (bcrypt.h)
description: Loads and initializes a CNG provider.
helpviewer_keywords: ["BCRYPT_ALG_HANDLE_HMAC_FLAG","BCRYPT_HASH_REUSABLE_FLAG","BCRYPT_PROV_DISPATCH","BCryptOpenAlgorithmProvider","BCryptOpenAlgorithmProvider function [Security]","MS_PRIMITIVE_PROVIDER","MS_PLATFORM_CRYPTO_PROVIDER","bcrypt/BCryptOpenAlgorithmProvider","security.bcryptopenalgorithmprovider_func"]
old-location: security\bcryptopenalgorithmprovider_func.htm
tech.root: security
ms.assetid: aceba9c0-19e6-4f3c-972a-752feed4a9f8
ms.date: 06/16/2025
ms.keywords: BCRYPT_ALG_HANDLE_HMAC_FLAG, BCRYPT_HASH_REUSABLE_FLAG, BCRYPT_PROV_DISPATCH, BCryptOpenAlgorithmProvider, BCryptOpenAlgorithmProvider function [Security], MS_PRIMITIVE_PROVIDER, MS_PLATFORM_CRYPTO_PROVIDER, bcrypt/BCryptOpenAlgorithmProvider, security.bcryptopenalgorithmprovider_func
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
 - BCryptOpenAlgorithmProvider
 - bcrypt/BCryptOpenAlgorithmProvider
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
 - BCryptOpenAlgorithmProvider
---

# BCryptOpenAlgorithmProvider function


## -description

The **BCryptOpenAlgorithmProvider** function loads and initializes a CNG algorithm provider.

**Note:** Callers targeting Windows 10 and later should consider using [CNG Algorithm Pseudo-handles](/windows/win32/seccng/cng-algorithm-pseudo-handles) instead of opening and closing CNG algorithm providers. See remarks of the CNG Algorithm Pseudo-handle documentation for restrictions.

## -parameters

### -param phAlgorithm [out]

A pointer to a **BCRYPT_ALG_HANDLE** variable that receives the CNG provider handle. When you have finished using this handle, release it by passing it to the [BCryptCloseAlgorithmProvider](nf-bcrypt-bcryptclosealgorithmprovider.md) function.

### -param pszAlgId [in]

A pointer to a null-terminated Unicode string that identifies the requested cryptographic algorithm. This can be one of the standard [CNG Algorithm Identifiers](/windows/win32/SecCNG/cng-algorithm-identifiers) or the identifier for another registered algorithm.

### -param pszImplementation [in, optional]

A pointer to a null-terminated Unicode string that identifies the specific provider to load. This is the registered alias of the cryptographic primitive provider. This parameter is optional and can be `NULL` if it is not needed. If this parameter is `NULL`, the default provider for the specified algorithm will be loaded.

> [!NOTE]
> If the *pszImplementation* parameter value is `NULL`, CNG attempts to open each registered provider, in order of priority, for the algorithm specified by the *pszAlgId* parameter and returns the handle of the first provider that is successfully opened. For the lifetime of the handle, any BCrypt*** cryptographic APIs will use the provider that was successfully opened.

**Windows Server 2008 and Windows Vista:** CNG attempts to fall back to the Microsoft CNG provider.

The following are the predefined provider names.

| Value | Meaning |
|-------|---------|
| **MS_PRIMITIVE_PROVIDER**<br/>L"Microsoft Primitive Provider" | Identifies the basic Microsoft CNG provider. |

### -param dwFlags [in]

Flags that modify the behavior of the function. This can be zero or a combination of one or more of the following values:

| Value | Meaning |
|-------|---------|
| **BCRYPT_ALG_HANDLE_HMAC_FLAG** | The provider will perform the [Hash-Based Message Authentication Code](/windows/win32/SecGloss/h-gly) (HMAC) algorithm with the specified hash algorithm. This flag is only used by hash algorithm providers. |
| **BCRYPT_PROV_DISPATCH** | Loads the provider into the nonpaged memory pool. If this flag is not present, the provider is loaded into the paged memory pool. When this flag is specified, the handle returned must not be closed before all dependent objects have been freed.</br></br>**Note:** This flag is only supported in kernel mode and allows subsequent operations on the provider to be processed at the Dispatch level. If the provider does not support being called at dispatch level, then it will return an error when opened using this flag.</br></br>**Windows Server 2008 and Windows Vista:** This flag is only supported by the Microsoft algorithm providers and only for [hashing algorithms](/windows/win32/SecGloss/h-gly) and [symmetric key](/windows/win32/SecGloss/s-gly) [cryptographic algorithms](/windows/win32/SecGloss/c-gly). |
| **BCRYPT_HASH_REUSABLE_FLAG** | Creates a hashing algorithm which has reusable hash objects. Hash objects for these algorithms can be used for a new hashing operation immediately after calling [BCryptFinishHash](nf-bcrypt-bcryptfinishhash.md). For more information, see [Creating a Hash with CNG](/windows/win32/SecCNG/creating-a-hash-with-cng).</br></br>**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This flag is not supported. |


## -returns

Returns a status code that indicates the success or failure of the function.

Possible return codes include, but are not limited to, the following:

| Return code | Description |
|-------------|-------------|
| **STATUS_SUCCESS** | The function was successful. |
| **STATUS_NOT_FOUND** | No provider was found for the specified algorithm ID. |
| **STATUS_INVALID_PARAMETER** | One of the supplied parameters is invalid. |
| **STATUS_NO_MEMORY** | A memory allocation failure occurred. |
| **STATUS_NOT_SUPPORTED** | One of the supplied flags is not supported for the specified algorithm ID. |

## -remarks

Because of the number and type of operations that are required to find, load, and initialize an algorithm provider, the **BCryptOpenAlgorithmProvider** function is a relatively time intensive function. Because of this, we recommend that you use [CNG Algorithm Pseudo-handles](/windows/win32/seccng/cng-algorithm-pseudo-handles) when possible, or cache any algorithm provider handles that you will use more than once, rather than opening and closing the algorithm providers repeatedly.

**BCryptOpenAlgorithmProvider** can be called either from user mode or kernel mode. Kernel mode callers must be executing at **PASSIVE_LEVEL** [IRQL](/windows/win32/SecGloss/i-gly).

To call this function in kernel mode, use `Cng.lib`, which is part of the Driver Development Kit (DDK). **Windows Server 2008 and Windows Vista:** To call this function in kernel mode, use Ksecdd.lib.

Starting in Windows 10, CNG no longer automatically processes every update to the cryptography configuration. Certain changes, like adding a new default provider or changing the preference order of algorithm providers, may require a reboot. Because of this, you should reboot before calling **BCryptOpenAlgorithmProvider** with any newly configured provider.

## -see-also

[BCryptCloseAlgorithmProvider](nf-bcrypt-bcryptclosealgorithmprovider.md)

[CNG Algorithm Pseudo-handles](/windows/win32/seccng/cng-algorithm-pseudo-handles)

[CNG Algorithm Identifiers](/windows/win32/SecCNG/cng-algorithm-identifiers)
