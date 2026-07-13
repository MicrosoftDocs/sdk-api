---
UID: NF:bcrypt.BCryptDuplicateHash
title: BCryptDuplicateHash function (bcrypt.h)
description: Duplicates an existing hash or Message Authentication Code (MAC) object.
helpviewer_keywords: ["BCryptDuplicateHash","BCryptDuplicateHash function [Security]","bcrypt/BCryptDuplicateHash","security.bcryptduplicatehash_func"]
old-location: security\bcryptduplicatehash_func.htm
tech.root: security
ms.assetid: 451ff5dc-b66a-4e8e-a327-28b4ee618b74
ms.date: 07/02/2025
ms.keywords: BCryptDuplicateHash, BCryptDuplicateHash function [Security], bcrypt/BCryptDuplicateHash, security.bcryptduplicatehash_func
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
 - BCryptDuplicateHash
 - bcrypt/BCryptDuplicateHash
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
 - BCryptDuplicateHash
---

# BCryptDuplicateHash function


## -description

The **BCryptDuplicateHash** function duplicates an existing hash or [Message Authentication Code](/windows/win32/SecGloss/m-gly) (MAC) object. The duplicate object contains all state and data contained in the original object at the point of duplication.

## -parameters

### -param hHash [in]

The handle of the hash or MAC object to duplicate.

### -param phNewHash [out]

A pointer to a **BCRYPT_HASH_HANDLE** value that receives the handle that represents the duplicate hash or MAC object. This handle is used in subsequent hashing or MAC functions, such as the [BCryptHashData](nf-bcrypt-bcrypthashdata.md) function. When you have finished using this handle, release it by passing it to the [BCryptDestroyHash](nf-bcrypt-bcryptdestroyhash.md) function.

### -param pbHashObject [out, optional]

A pointer to a buffer that receives the duplicate hash or MAC object. The *cbHashObject* parameter contains the size of this buffer. The required size of this buffer can be obtained by calling the [BCryptGetProperty](nf-bcrypt-bcryptgetproperty.md) function to get the **BCRYPT_OBJECT_LENGTH** property from the algorithm or hash handle. This will provide the size of the hash or MAC object for the specified algorithm.

This memory can only be freed after the handle pointed to by the *phHash* parameter is destroyed.

If the value of this parameter is `NULL` and the value of the *cbHashObject* parameter is zero, the memory for the hash object is allocated by this function, and freed by [BCryptDestroyHash](nf-bcrypt-bcryptdestroyhash.md). **Windows 7:** This memory management functionality is available beginning with Windows 7.

### -param cbHashObject [in]

The size, in bytes, of the *pbHashObject* buffer.

If the value of this parameter is zero and the value of the *pbHashObject* parameter is `NULL`, the memory for the key object is allocated by this function, and freed by [BCryptDestroyHash](nf-bcrypt-bcryptdestroyhash.md). **Windows 7:** This memory management functionality is available beginning with Windows 7.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are currently defined, so this parameter should be zero.

## -returns

Returns a status code that indicates the success or failure of the function.

Possible return codes include, but are not limited to, the following.


| Return code | Description |
|-------------|-------------|
| **STATUS_SUCCESS** | The function was successful. |
| **STATUS_BUFFER_TOO_SMALL** | The size of the hash object specified by the *cbHashObject* parameter is not large enough to hold the hash object. |
| **STATUS_INVALID_HANDLE** | The handle in the *hHash* parameter is not valid. |
| **STATUS_INVALID_PARAMETER** | One or more parameters are not valid. |

## -remarks

This function is useful when computing a hash or MAC over a block of common data. After the common data has been processed, the hash or MAC object can be duplicated, and then the unique data can be added to the individual objects.

When using a supported algorithm provider, **BCryptDuplicateHash** can be called either from user mode or kernel mode. Kernel mode callers can execute either at **PASSIVE_LEVEL** [IRQL](/windows/win32/SecGloss/i-gly) or **DISPATCH_LEVEL** IRQL. If the current IRQL level is **DISPATCH_LEVEL**, the handle provided in the *hHash* parameter must be derived from an algorithm handle returned by a provider that was opened by using the **BCRYPT_PROV_DISPATCH** flag, and any pointers passed to the **BCryptDuplicateHash** function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use `Cng.lib`, which is part of the Driver Development Kit (DDK). **Windows Server 2008 and Windows Vista:** To call this function in kernel mode, use `Ksecdd.lib`.

## -see-also

[BCryptDuplicateHash](nf-bcrypt-bcryptduplicatehash.md)

[BCryptHashData](nf-bcrypt-bcrypthashdata.md)

[BCryptFinishHash](nf-bcrypt-bcryptfinishhash.md)

[BCryptDestroyHash](nf-bcrypt-bcryptdestroyhash.md)
