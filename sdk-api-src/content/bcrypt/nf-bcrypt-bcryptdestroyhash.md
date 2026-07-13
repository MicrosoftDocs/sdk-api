---
UID: NF:bcrypt.BCryptDestroyHash
title: BCryptDestroyHash function (bcrypt.h)
description: Destroys a hash or Message Authentication Code (MAC) object.
helpviewer_keywords: ["BCryptDestroyHash","BCryptDestroyHash function [Security]","bcrypt/BCryptDestroyHash","security.bcryptdestroyhash_func"]
old-location: security\bcryptdestroyhash_func.htm
tech.root: security
ms.assetid: 067dac61-98b9-478c-ac4d-e141961865e9
ms.date: 12/05/2018
ms.keywords: BCryptDestroyHash, BCryptDestroyHash function [Security], bcrypt/BCryptDestroyHash, security.bcryptdestroyhash_func
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
 - BCryptDestroyHash
 - bcrypt/BCryptDestroyHash
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
 - BCryptDestroyHash
---

# BCryptDestroyHash function


## -description

The **BCryptDestroyHash** function destroys a hash or [Message Authentication Code](/windows/win32/SecGloss/m-gly) (MAC) object.

## -parameters

### -param hHash [in, out]

The handle of the hash or MAC object to destroy. This handle is obtained by using the [BCryptCreateHash](nf-bcrypt-bcryptcreatehash.md) function.

## -returns

Returns a status code that indicates the success or failure of the function.

Possible return codes include, but are not limited to, the following:

| Return code | Description |
|-------------|-------------|
| **STATUS_SUCCESS** | The function was successful. |
| **STATUS_INVALID_HANDLE** | The algorithm handle in the *hHash* parameter is not valid. |

## -remarks

When using a supported algorithm provider, *BCryptDestroyHash* can be called either from user mode or kernel mode. Kernel mode callers can execute either at **PASSIVE_LEVEL** [IRQL](/windows/win32/SecGloss/i-gly) or **DISPATCH_LEVEL** IRQL. If the current IRQL level is **DISPATCH_LEVEL**, the handle provided in the *hHash* parameter must be derived from an algorithm handle returned by a provider that was opened by using the **BCRYPT_PROV_DISPATCH** flag.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). **Windows Server 2008 and Windows Vista:** To call this function in kernel mode, use Ksecdd.lib.

## -see-also

[BCryptCreateHash](nf-bcrypt-bcryptcreatehash.md)
