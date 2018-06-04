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

# _BCRYPT_MULTI_HASH_OPERATION structure


## -description


A <b>BCRYPT_MULTI_HASH_OPERATION</b> structure defines a single operation in a multi-hash operation.


## -struct-fields




### -field iHash

An index into the multi-object state array of the hash state on which this computation operates. The first element of the array corresponds to an <i>iHash</i> value of zero (0). Valid values are less than the value of the <i>nHashes</i> parameter of the <a href="https://msdn.microsoft.com/AAF91460-AEFB-4E16-91EA-4A60272B3839">BCryptCreateMultiHash</a> function.


### -field hashOperation

A hash operation type, either <b>BCRYPT_HASH_OPERATION_HASH_DATA</b> or <b>BCRYPT_HASH_OPERATION_FINISH_HASH</b>.

If the value is <b>BCRYPT_HASH_OPERATION_HASH_DATA</b>, the operation performed is  equivalent to calling the <a href="https://msdn.microsoft.com/dab89dff-dc84-4f69-8b6b-de65704b0265">BCryptHashData</a> function on the hash object array element with <i>pbBuffer</i>/<i>cbBuffer</i> pointing to the buffer to be hashed.

If the value is <b>BCRYPT_HASH_OPERATION_FINISH_HASH</b>, the operation performed is  equivalent to calling the <a href="https://msdn.microsoft.com/82a7c3d9-c01b-46d0-8b54-694dc0d8ffdd">BCryptFinishHash</a> function on the hash object array element with <i>pbBuffer</i>/<i>cbBuffer</i> pointing to the output buffer that receives the result.


### -field pbBuffer

The buffer on which the operation works.


### -field cbBuffer

The buffer on which the operation works.


## -see-also




<a href="https://msdn.microsoft.com/AAF91460-AEFB-4E16-91EA-4A60272B3839">BCryptCreateMultiHash</a>



<a href="https://msdn.microsoft.com/82a7c3d9-c01b-46d0-8b54-694dc0d8ffdd">BCryptFinishHash</a>



<a href="https://msdn.microsoft.com/dab89dff-dc84-4f69-8b6b-de65704b0265">BCryptHashData</a>
 

 

