---
UID: NF:bcrypt.BCryptCreateMultiHash
title: BCryptCreateMultiHash function (bcrypt.h)
author: windows-sdk-content
description: The BCryptCreateMultiHash function creates a multi-hash state that allows for the parallel computation of multiple hash operations.
old-location: security\bcryptcreatemultihash.htm
tech.root: SecCNG
ms.assetid: AAF91460-AEFB-4E16-91EA-4A60272B3839
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BCRYPT_HASH_REUSABLE_FLAG, BCryptCreateMultiHash, BCryptCreateMultiHash function [Security], bcrypt/BCryptCreateMultiHash, security.bcryptcreatemultihash
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BCryptCreateMultiHash function


## -description


The <b>BCryptCreateMultiHash</b> function creates a multi-hash state that allows for the parallel computation of multiple hash operations. This multi-hash state is used by the <a href="https://msdn.microsoft.com/en-us/library/Mt845764(v=VS.85).aspx">BCryptProcessMultiOperations</a> function. The multi-hash state can be thought of as an array of hash objects, each of which is equivalent to one created by <a href="https://msdn.microsoft.com/deb02f67-f3d3-4542-8245-fd4982c3190b">BCryptCreateHash</a>.

 Parallel computations can greatly increase overall throughput, at the expense of increased latency for individual computations.

 Parallel hash computations are currently only implemented for SHA-256, SHA-384, and SHA-512. Other hash algorithms can be used with the parallel computation API but they run at the throughput of the sequential hash operations. The set of hash algorithms that can benefit from parallel computations might change in future updates.


## -parameters




### -param hAlgorithm [in, out]

The algorithm handle used for all of the hash states in the multi-hash array. The algorithm handle must have been opened with the <b>BCYRPT_MULTI_FLAG</b> passed to the <a href="https://msdn.microsoft.com/aceba9c0-19e6-4f3c-972a-752feed4a9f8">BCryptOpenAlgorithmProvider</a> function. Alternatively, the caller can use the pseudo-handles. 


### -param phHash [out]

A pointer to a <b>BCRYPT_HASH_HANDLE</b> value that receives a handle that represents the multi-hash state. This handle is used in subsequent operations such as <a href="https://msdn.microsoft.com/en-us/library/Mt845764(v=VS.85).aspx">BCryptProcessMultiOperations</a>. When you have finished using this handle, release it by passing it to the <a href="https://msdn.microsoft.com/067dac61-98b9-478c-ac4d-e141961865e9">BCryptDestroyHash</a> function.


### -param nHashes [in]

The number of elements in the array. The multi-hash state that this function creates is able to perform parallel computations on <i>nHashes</i> different hash states.


### -param pbHashObject [out]

A pointer to a buffer that receives the multi-hash state. 

The size can be calculated from the <b>cbPerObject</b>  and <b>cbPerElement</b> members of the <a href="https://msdn.microsoft.com/en-us/library/Mt845767(v=VS.85).aspx">BCRYPT_MULTI_OBJECT_LENGTH_STRUCT</a> structure. The value is the following: <code>cbPerObject + (number of hash states) * cbPerElement</code>.

If <i>pbHashObject</i> is <b>NULL</b> and <i>cbHashObject</i> has a value of zero (0), the object buffer is automatically allocated.


### -param cbHashObject [in]

The size of the <i>pbHashObject</i> buffer, or zero if <i>pbHashObject</i> is <b>NULL</b>.


### -param pbSecret [in]

A pointer to a buffer that contains the key to use for the hash or MAC. The <i>cbSecret</i> parameter contains the size of this buffer. This key only applies to hash algorithms opened by the <a href="https://msdn.microsoft.com/aceba9c0-19e6-4f3c-972a-752feed4a9f8">BCryptOpenAlgorithmProvider</a> function by using the <b>BCRYPT_ALG_HANDLE_HMAC</b> flag.  Otherwise, set this parameter to <b>NULL</b>. 

The same key is used for all elements of the array.


### -param cbSecret [in]

The size, in bytes, of the <i>pbSecret</i> buffer. If no key is used, set this parameter to zero.


### -param dwFlags [in]

Flags that modify the behavior of the function. This can be zero or the values below. Multi-hash objects are always reusable and always behave as if the <b>BCRYPT_HASH_REUSABLE_FLAG</b> was passed. This flag is supported here for consistency.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_HASH_REUSABLE_FLAG"></a><a id="bcrypt_hash_reusable_flag"></a><dl>
<dt><b>BCRYPT_HASH_REUSABLE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Creates a reusable hashing object. The object can be used for a new hashing operation immediately after calling <a href="https://msdn.microsoft.com/82a7c3d9-c01b-46d0-8b54-694dc0d8ffdd">BCryptFinishHash</a>. For more information, see <a href="https://msdn.microsoft.com/f36b7e36-4377-4940-8951-6caba6e3ce8a">Creating a Hash with CNG</a>.

</td>
</tr>
</table>
 


## -remarks



 Internally, parallel hash computations are done using single-instruction multiple-data (SIMD) instructions with up to 8 parallel computations at a time, depending on the hash algorithm and the CPU features available. To maximize performance, we recommend that the caller provide at least eight computations that can be processed in parallel. 

For computations of unequal length, providing more computations in parallel allows the implementation to schedule the computations better across the CPU registers. This can provide a throughput benefit. For optimal throughput, we recommend that the caller provide between eight and 100 computations. Select a lower value in that range only if all the hash computations are the same length.

Multi-hashing is not supported for HMAC-MD2, HMAC-MD4, and GMAC.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt845767(v=VS.85).aspx">BCRYPT_MULTI_OBJECT_LENGTH</a>



<a href="https://msdn.microsoft.com/deb02f67-f3d3-4542-8245-fd4982c3190b">BCryptCreateHash</a>



<a href="https://msdn.microsoft.com/067dac61-98b9-478c-ac4d-e141961865e9">BCryptDestroyHash</a>



<a href="https://msdn.microsoft.com/82a7c3d9-c01b-46d0-8b54-694dc0d8ffdd">BCryptFinishHash</a>



<a href="https://msdn.microsoft.com/dab89dff-dc84-4f69-8b6b-de65704b0265">BCryptHashData</a>



<a href="https://msdn.microsoft.com/aceba9c0-19e6-4f3c-972a-752feed4a9f8">BCryptOpenAlgorithmProvider</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt845764(v=VS.85).aspx">BCryptProcessMultiOperations</a>



<a href="https://msdn.microsoft.com/f36b7e36-4377-4940-8951-6caba6e3ce8a">Creating a Hash with CNG</a>
 

 

