---
UID: NF:bcrypt.BCryptProcessMultiOperations
title: BCryptProcessMultiOperations function (bcrypt.h)
description: The BCryptProcessMultiOperations function processes a sequence of operations on a multi-object state.
helpviewer_keywords: ["BCryptProcessMultiOperations","BCryptProcessMultiOperations function [Security]","bcrypt/BCryptProcessMultiOperations","security.bcryptprocessmultioperation"]
old-location: security\bcryptprocessmultioperation.htm
tech.root: security
ms.assetid: 5FD28AC3-46D2-4F06-BF06-F5FEF8E531F5
ms.date: 03/21/2023
ms.keywords: BCryptProcessMultiOperations, BCryptProcessMultiOperations function [Security], bcrypt/BCryptProcessMultiOperations, security.bcryptprocessmultioperation
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 Update [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 Update [desktop apps \| UWP apps]
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
 - BCryptProcessMultiOperations
 - bcrypt/BCryptProcessMultiOperations
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
 - BCryptProcessMultiOperations
---

# BCryptProcessMultiOperations function

## -description

The **BCryptProcessMultiOperations** function processes a sequence of operations on a multi-object state.

## -parameters

### -param hObject

*BCRYPT_HANDLE* `[in, out]`

A handle to a multi-object state, such as one created by the [BCryptCreateMultiHash](nf-bcrypt-bcryptcreatemultihash.md) function.

### -param operationType

*BCRYPT_MULTI_OPERATION_TYPE* `[in]`

One of the **BCRYPT_OPERATION_TYPE_**\* values. Currently the only defined value is **BCRYPT_OPERATION_TYPE_HASH**. This value identifies the *hObject* parameter as a multi-hash object and the *pOperations* pointer as pointing to an array of [BCRYPT_MULTI_HASH_OPERATION](ns-bcrypt-bcrypt_multi_hash_operation.md) elements.

### -param pOperations

*PVOID* `[in]`

A pointer to an array of operation command structures. For hashing, it is a pointer to an array of [BCRYPT_MULTI_HASH_OPERATION](ns-bcrypt-bcrypt_multi_hash_operation.md) structures.

### -param cbOperations

*ULONG* `[in]`

The size, in bytes, of the *pOperations* array.

### -param dwFlags

*ULONG* `[in]`

Specify a value of zero (`0`).

## -returns

Returns a status code that indicates the success or failure of the function. If the method succeeds, it will return `STATUS_SUCCESS`. For other **NTSTATUS** values, see [NTSTATUS Values](/openspecs/windows_protocols/ms-erref/596a1078-e883-4972-9bbc-49e60bebca55).

## -remarks

Each element of the *pOperations* array contains instructions for a particular computation to be performed on a single element of the multi-object state. The functional behavior of **BCryptProcessMultiOperations** is equivalent to performing, for each element in the multi-object state, the computations specified in the operations array for that element, one at a time, in order.

The relative order of two operations that operate on different elements of the array is not guaranteed. If an output buffer overlaps an input or output buffer the result is not deterministic.

## -see-also

[BCRYPT_MULTI_HASH_OPERATION](ns-bcrypt-bcrypt_multi_hash_operation.md)

[BCryptCreateMultiHash](nf-bcrypt-bcryptcreatemultihash.md)
