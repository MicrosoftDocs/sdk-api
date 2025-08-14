---
UID: NF:bcrypt.BCryptCloseAlgorithmProvider
title: BCryptCloseAlgorithmProvider function (bcrypt.h)
description: Closes an algorithm provider.
helpviewer_keywords: ["BCryptCloseAlgorithmProvider","BCryptCloseAlgorithmProvider function [Security]","bcrypt/BCryptCloseAlgorithmProvider","security.bcryptclosealgorithmprovider_func"]
old-location: security\bcryptclosealgorithmprovider_func.htm
tech.root: security
ms.assetid: def90d52-87e0-40e6-9c50-fd77177991d0
ms.date: 06/16/2025
ms.keywords: BCryptCloseAlgorithmProvider, BCryptCloseAlgorithmProvider function [Security], bcrypt/BCryptCloseAlgorithmProvider, security.bcryptclosealgorithmprovider_func
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
 - BCryptCloseAlgorithmProvider
 - bcrypt/BCryptCloseAlgorithmProvider
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
 - BCryptCloseAlgorithmProvider
---

# BCryptCloseAlgorithmProvider function


## -description

The **BCryptCloseAlgorithmProvider** function closes a CNG algorithm provider.

**Note:** Callers targeting Windows 10 and later should consider using [CNG Algorithm Pseudo-handles](/windows/win32/seccng/cng-algorithm-pseudo-handles) instead of opening and closing CNG algorithm providers. See remarks of the CNG Algorithm Pseudo-handle documentation for restrictions.

## -parameters

### -param hAlgorithm [in, out]

A handle that represents the algorithm provider to close. This handle is obtained by calling the [BCryptOpenAlgorithmProvider](nf-bcrypt-bcryptopenalgorithmprovider.md) function.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are defined for this function.

## -returns

Returns a status code that indicates the success or failure of the function.

Possible return codes include, but are not limited to, the following.

| Return code | Description |
|-------------|-------------|
| **STATUS_SUCCESS** | The function was successful. |
| **STATUS_INVALID_HANDLE** | The algorithm handle specified by the *hAlgorithm* parameter is not valid, or is a pseudo-handle which cannot be closed. |

## -remarks

**BCryptCloseAlgorithmProvider** can be called either from user mode or kernel mode. Kernel mode callers must be executing at **PASSIVE_LEVEL** [IRQL](/windows/win32/SecGloss/i-gly).

To call this function in kernel mode, use `Cng.lib`, which is part of the Driver Development Kit (DDK). **Windows Server 2008 and Windows Vista:** To call this function in kernel mode, use `Ksecdd.lib`.

## -see-also

[BCryptOpenAlgorithmProvider](nf-bcrypt-bcryptopenalgorithmprovider.md)

[CNG Algorithm Pseudo-handles](/windows/win32/seccng/cng-algorithm-pseudo-handles)
