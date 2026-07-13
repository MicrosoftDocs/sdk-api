---
UID: NF:bcrypt.BCryptCreateMultiHash
title: BCryptCreateMultiHash function (bcrypt.h)
description: The BCryptCreateMultiHash function creates a multi-hash state that allows for the parallel computation of multiple hash operations.
helpviewer_keywords: ["BCRYPT_HASH_REUSABLE_FLAG","BCryptCreateMultiHash","BCryptCreateMultiHash function [Security]","bcrypt/BCryptCreateMultiHash","security.bcryptcreatemultihash"]
old-location: security\bcryptcreatemultihash.htm
tech.root: security
ms.assetid: AAF91460-AEFB-4E16-91EA-4A60272B3839
ms.date: 03/21/2023
ms.keywords: BCRYPT_HASH_REUSABLE_FLAG, BCryptCreateMultiHash, BCryptCreateMultiHash function [Security], bcrypt/BCryptCreateMultiHash, security.bcryptcreatemultihash
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
 - BCryptCreateMultiHash
 - bcrypt/BCryptCreateMultiHash
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
 - BCryptCreateMultiHash
---

# BCryptCreateMultiHash function

## -description

The **BCryptCreateMultiHash** function creates a multi-hash state that allows for the parallel computation of multiple hash operations. This multi-hash state is used by the [BCryptProcessMultiOperations](nf-bcrypt-bcryptprocessmultioperations.md) function. The multi-hash state can be thought of as an array of hash objects, each of which is equivalent to one created by [BCryptCreateHash](nf-bcrypt-bcryptcreatehash.md).

 Parallel computations can greatly increase overall throughput, at the expense of increased latency for individual computations.

 Parallel hash computations are currently only implemented for SHA-256, SHA-384, and SHA-512. Other hash algorithms can be used with the parallel computation API but they run at the throughput of the sequential hash operations. The set of hash algorithms that can benefit from parallel computations might change in future updates.

## -parameters

### -param hAlgorithm

*BCRYPT_ALG_HANDLE* `[in, out]`

The algorithm handle used for all of the hash states in the multi-hash array. The algorithm handle must have been opened with the **BCYRPT_MULTI_FLAG** passed to the [BCryptOpenAlgorithmProvider](nf-bcrypt-bcryptopenalgorithmprovider.md) function. Alternatively, the caller can use the pseudo-handles.

### -param phHash

*BCRYPT_HASH_HANDLE** `[out]`

A pointer to a **BCRYPT_HASH_HANDLE** value that receives a handle that represents the multi-hash state. This handle is used in subsequent operations such as [BCryptProcessMultiOperations](nf-bcrypt-bcryptprocessmultioperations.md). When you have finished using this handle, release it by passing it to the [BCryptDestroyHash](nf-bcrypt-bcryptdestroyhash.md) function.

### -param nHashes

*ULONG* `[in]`

The number of elements in the array. The multi-hash state that this function creates is able to perform parallel computations on *nHashes* different hash states.

### -param pbHashObject

*PUCHAR* `[out]`

A pointer to a buffer that receives the multi-hash state.

The size can be calculated from the **cbPerObject** and **cbPerElement** members of the [BCRYPT_MULTI_OBJECT_LENGTH_STRUCT](ns-bcrypt-bcrypt_multi_object_length_struct.md) structure. The value is the following: `cbPerObject + (number of hash states) * cbPerElement`.

If *pbHashObject* is `NULL` and *cbHashObject* has a value of zero (`0`), the object buffer is automatically allocated.

### -param cbHashObject

*ULONG* `[in]`

The size of the *pbHashObject* buffer, or zero (`0`) if *pbHashObject* is `NULL`.

### -param pbSecret

*PUCHAR* `[in]`

A pointer to a buffer that contains the key to use for the hash or MAC. The *cbSecret* parameter contains the size of this buffer. This key only applies to hash algorithms opened by the [BCryptOpenAlgorithmProvider](nf-bcrypt-bcryptopenalgorithmprovider.md) function by using the **BCRYPT_ALG_HANDLE_HMAC** flag. Otherwise, set this parameter to `NULL`.

The same key is used for all elements of the array.

### -param cbSecret

*ULONG* `[in]`

The size, in bytes, of the *pbSecret* buffer. If no key is used, set this parameter to zero (`0`).

### -param dwFlags

*ULONG* `[in]`

Flags that modify the behavior of the function. This can be zero or the values below. Multi-hash objects are always reusable and always behave as if the **BCRYPT_HASH_REUSABLE_FLAG** was passed. This flag is supported here for consistency.

| Value | Meaning |
|--------|--------|
| **BCRYPT_HASH_REUSABLE_FLAG** | Creates a reusable hashing object. The object can be used for a new hashing operation immediately after calling [BCryptFinishHash](nf-bcrypt-bcryptfinishhash.md). For more information, see [Creating a Hash with CNG](/windows/win32/SecCNG/creating-a-hash-with-cng). |

## -returns

Returns a status code that indicates the success or failure of the function. If the method succeeds, it will return `STATUS_SUCCESS`. For other **NTSTATUS** values, see [NTSTATUS Values](/openspecs/windows_protocols/ms-erref/596a1078-e883-4972-9bbc-49e60bebca55).

## -remarks

 Internally, parallel hash computations are done using single-instruction multiple-data (SIMD) instructions with up to 8 parallel computations at a time, depending on the hash algorithm and the CPU features available. To maximize performance, we recommend that the caller provide at least eight computations that can be processed in parallel.

For computations of unequal length, providing more computations in parallel allows the implementation to schedule the computations better across the CPU registers. This can provide a throughput benefit. For optimal throughput, we recommend that the caller provide between eight and 100 computations. Select a lower value in that range only if all the hash computations are the same length.

Multi-hashing is not supported for HMAC-MD2, HMAC-MD4, and GMAC.

## -see-also

[BCRYPT_MULTI_OBJECT_LENGTH](ns-bcrypt-bcrypt_multi_object_length_struct.md)

[BCryptCreateHash](nf-bcrypt-bcryptcreatehash.md)

[BCryptDestroyHash](nf-bcrypt-bcryptdestroyhash.md)

[BCryptFinishHash](nf-bcrypt-bcryptfinishhash.md)

[BCryptHashData](nf-bcrypt-bcrypthashdata.md)

[BCryptOpenAlgorithmProvider](nf-bcrypt-bcryptopenalgorithmprovider.md)

[BCryptProcessMultiOperations](nf-bcrypt-bcryptprocessmultioperations.md)

[Creating a Hash with CNG](/windows/win32/SecCNG/creating-a-hash-with-cng)
