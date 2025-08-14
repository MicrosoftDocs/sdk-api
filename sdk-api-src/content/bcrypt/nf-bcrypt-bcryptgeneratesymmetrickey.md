---
UID: NF:bcrypt.BCryptGenerateSymmetricKey
title: BCryptGenerateSymmetricKey function (bcrypt.h)
description: Creates a key object for use with a symmetrical key encryption algorithm from a supplied key.
helpviewer_keywords: ["BCryptGenerateSymmetricKey","BCryptGenerateSymmetricKey function [Security]","bcrypt/BCryptGenerateSymmetricKey","security.bcryptgeneratesymmetrickey_func"]
old-location: security\bcryptgeneratesymmetrickey_func.htm
tech.root: security
ms.assetid: c55d714f-f47e-4ddf-97b9-985c0441bb2d
ms.date: 06/30/2025
ms.keywords: BCryptGenerateSymmetricKey, BCryptGenerateSymmetricKey function [Security], bcrypt/BCryptGenerateSymmetricKey, security.bcryptgeneratesymmetrickey_func
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
 - BCryptGenerateSymmetricKey
 - bcrypt/BCryptGenerateSymmetricKey
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
 - BCryptGenerateSymmetricKey
---

# BCryptGenerateSymmetricKey function


## -description

The **BCryptGenerateSymmetricKey** function creates a key object for use with an algorithm which uses symmetric keys, using supplied secret key data.

## -parameters

### -param hAlgorithm [in, out]

The handle of an algorithm provider that uses symmetric keys. Examples of types of algorithms include Ciphers, and Key Derivation Functions (KDF). This handle is obtained by calling the [BCryptOpenAlgorithmProvider](nf-bcrypt-bcryptopenalgorithmprovider.md) function, or may be a [CNG Algorithm Pseudo-handle](/windows/win32/seccng/cng-algorithm-pseudo-handles).

### -param phKey [out]

A pointer to a **BCRYPT_KEY_HANDLE** that receives the handle of the key. This handle is used in subsequent functions that require a symmetric key, such as [BCryptEncrypt](nf-bcrypt-bcryptencrypt.md) and [BCryptKeyDerivation](nf-bcrypt-bcryptkeyderivation.md). This handle must be released when it is no longer needed by passing it to the [BCryptDestroyKey](nf-bcrypt-bcryptdestroykey.md) function.

### -param pbKeyObject [out, optional]

A pointer to a buffer that receives the key object. The *cbKeyObject* parameter contains the size of this buffer. The required size of this buffer can be obtained by calling the [BCryptGetProperty](nf-bcrypt-bcryptgetproperty.md) function to get the **BCRYPT_OBJECT_LENGTH** property from the algorithm handle. This will provide the size of the key object for the specified algorithm.

This memory can only be freed after the *phKey* key handle is destroyed.

If the value of this parameter is `NULL` and the value of the *cbKeyObject* parameter is zero, the memory for the key object is allocated by this function, and freed by [BCryptDestroyKey](nf-bcrypt-bcryptdestroykey.md). **Windows 7:** This memory management functionality is available beginning with Windows 7.

### -param cbKeyObject [in]

The size, in bytes, of the *pbKeyObject* buffer.

If the value of this parameter is zero and the value of the *pbKeyObject* parameter is `NULL`, the memory for the key object is allocated by this function, and freed by [BCryptDestroyKey](nf-bcrypt-bcryptdestroykey.md). **Windows 7:** This memory management functionality is available beginning with Windows 7.

### -param pbSecret [in]

Pointer to a buffer that contains the key data from which to create the key object. The *cbSecret* parameter contains the size of this buffer. This is normally the result of a call to [BCryptDeriveKey](nf-bcrypt-bcryptderivekey.md) or some other reproducible secret data. If the data passed in exceeds the target key size, the data will be truncated and the excess will be ignored.

> [!NOTE]
> We strongly recommended that applications pass in the exact number of bytes required by the target key.

### -param cbSecret [in]

The size, in bytes, of the *pbSecret* buffer.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are currently defined, so this parameter should be zero.

## -returns

Returns a status code that indicates the success or failure of the function.

Possible return codes include, but are not limited to, the following:


| Return code | Description |
|-------------|-------------|
| **STATUS_SUCCESS** | The function was successful. |
| **STATUS_BUFFER_TOO_SMALL** | The size of the key object specified by the *cbKeyObject* parameter is not large enough to hold the key object. |
| **STATUS_INVALID_HANDLE** | The algorithm handle in the *hAlgorithm* parameter is not valid. |
| **STATUS_INVALID_PARAMETER** | One or more parameters are not valid. |

## -remarks

When using a supported algorithm provider, *BCryptGenerateSymmetricKey* can be called either from user mode or kernel mode. Kernel mode callers can execute either at **PASSIVE_LEVEL** [IRQL](/windows/win32/SecGloss/i-gly) or **DISPATCH_LEVEL** IRQL. If the current IRQL level is **DISPATCH_LEVEL**, the handle provided in the *hAlgorithm* parameter must have been opened by using the **BCRYPT_PROV_DISPATCH** flag, and any pointers passed to the *BCryptGenerateSymmetricKey* function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use `Cng.lib`, which is part of the Driver Development Kit (DDK). **Windows Server 2008 and Windows Vista:** To call this function in kernel mode, use Ksecdd.lib.

## -see-also

[BCryptDestroyKey](nf-bcrypt-bcryptdestroykey.md)
