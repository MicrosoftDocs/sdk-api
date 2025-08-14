---
UID: NF:bcrypt.BCryptHashData
title: BCryptHashData function (bcrypt.h)
description: Performs a one way hash or Message Authentication Code (MAC) on a data buffer.
helpviewer_keywords: ["BCryptHashData","BCryptHashData function [Security]","bcrypt/BCryptHashData","security.bcrypthashdata_func"]
old-location: security\bcrypthashdata_func.htm
tech.root: security
ms.assetid: dab89dff-dc84-4f69-8b6b-de65704b0265
ms.date: 07/01/2025
ms.keywords: BCryptHashData, BCryptHashData function [Security], bcrypt/BCryptHashData, security.bcrypthashdata_func
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
 - BCryptHashData
 - bcrypt/BCryptHashData
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
 - BCryptHashData
---

# BCryptHashData function


## -description

The **BCryptHashData** function appends data to an ongoing cryptographic hash or [Message Authentication Code](/windows/win32/SecGloss/m-gly) (MAC) computation.

## -parameters

### -param hHash [in, out]

The handle of the hash or MAC object to use to perform the operation. This handle is obtained by calling the [BCryptCreateHash](nf-bcrypt-bcryptcreatehash.md) or [BCryptDuplicateHash](nf-bcrypt-bcryptduplicatehash.md) functions.

### -param pbInput [in]

A pointer to a buffer that contains the data to process. The *cbInput* parameter contains the number of bytes in this buffer. This function does not modify the contents of this buffer.

### -param cbInput [in]

The size, in bytes, of the *pbInput* buffer.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are currently defined, so this parameter should be zero.

## -returns

Returns a status code that indicates the success or failure of the function.

Possible return codes include, but are not limited to, the following.

| Return code | Description |
|-------------|-------------|
| **STATUS_SUCCESS** | The function was successful. |
| **STATUS_INVALID_PARAMETER** | One or more parameters are not valid. |
| **STATUS_INVALID_HANDLE** | The handle in the *hHash* parameter is not valid. After the [BCryptFinishHash](nf-bcrypt-bcryptfinishhash.md) function has been called, that handle cannot be reused, unless the handle was created with the **BCRYPT_HASH_REUSABLE_FLAG** flag. |

## -remarks

To combine more than one buffer into the hash or MAC, you can call this function multiple times, passing a different buffer each time. This is functionally equivalent to concatenating these buffers into a single buffer and doing a single hash or MAC call, but is more often more convenient when the data is not naturally contiguous in memory.

To obtain the hash or MAC value, call the [BCryptFinishHash](nf-bcrypt-bcryptfinishhash.md) function. After the [BCryptFinishHash](nf-bcrypt-bcryptfinishhash.md) function has been called, the *hHash* handle cannot be reused, unless it was created with the **BCRYPT_HASH_REUSABLE_FLAG** flag.

When using a supported algorithm provider, **BCryptHashData** can be called either from user mode or kernel mode. Kernel mode callers can execute either at **PASSIVE_LEVEL** [IRQL](/windows/win32/SecGloss/i-gly) or **DISPATCH_LEVEL** IRQL. If the current IRQL level is **DISPATCH_LEVEL**, the handle provided in the *hAlgorithm* parameter must have been opened by using the **BCRYPT_PROV_DISPATCH** flag, and any pointers passed to the **BCryptHashData** function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use `Cng.lib`, which is part of the Driver Development Kit (DDK). **Windows Server 2008 and Windows Vista:** To call this function in kernel mode, use `Ksecdd.lib`.

## -see-also

[BCryptCreateHash](nf-bcrypt-bcryptcreatehash.md)

[BCryptFinishHash](nf-bcrypt-bcryptfinishhash.md)

[BCryptDestroyHash](nf-bcrypt-bcryptdestroyhash.md)
