---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# BCryptProcessMultiOperations function


## -description


The <b>BCryptProcessMultiOperations</b> function processes a sequence of operations on a multi-object state.


## -parameters




### -param hObject [in, out]

A handle to a multi-object state, such as one created by the <a href="https://msdn.microsoft.com/AAF91460-AEFB-4E16-91EA-4A60272B3839">BCryptCreateMultiHash</a> function.


### -param operationType [in]

A <b>BCRYPT_OPERATION_TYPE_*</b> value. Currently the only defined value is <b>BCRYPT_OPERATION_TYPE_HASH</b>. This value identifies the <i>hObject</i> parameter as a multi-hash object and the <i>pOperations</i> pointer as pointing to an array of <a href="https://msdn.microsoft.com/B0418A07-D2EE-4346-9971-676C8FB08FAA">BCRYPT_MULTI_HASH_OPERATION</a> elements.


### -param pOperations [in]

A pointer to an array of operation command structures. For hashing, it is a pointer to an array of <a href="https://msdn.microsoft.com/B0418A07-D2EE-4346-9971-676C8FB08FAA">BCRYPT_MULTI_HASH_OPERATION</a> structures.


### -param cbOperations [in]

The size, in bytes, of the <i>pOperations</i> array.


### -param dwFlags [in]

Specify a value of zero (0).


## -remarks



Each element of the <i>pOperations</i> array contains instructions for a particular computation to be performed on a single element of the multi-object state. The functional behavior of <b>BCryptProcessMultiOperations</b> is equivalent to performing, for each element in the multi-object state, the computations specified in the operations array for that element, one at a time, in order. 

The relative order of two operations that operate on different elements of the array is not guaranteed. If an output buffer overlaps an input or output buffer the result is not deterministic.




## -see-also




<a href="https://msdn.microsoft.com/B0418A07-D2EE-4346-9971-676C8FB08FAA">BCRYPT_MULTI_HASH_OPERATION</a>



<a href="https://msdn.microsoft.com/AAF91460-AEFB-4E16-91EA-4A60272B3839">BCryptCreateMultiHash</a>
 

 

