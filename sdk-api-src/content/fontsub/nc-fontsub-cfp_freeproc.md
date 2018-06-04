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

# CFP_FREEPROC callback function


## -description



      
      Client-provided callback function, used by <a href="https://msdn.microsoft.com/aeea47c7-af55-46c4-b701-e00ec7540d24">CreateFontPackage</a> and <a href="https://msdn.microsoft.com/c51110a0-286c-4d97-9da5-4186ebf8f9b8">MergeFontPackage</a> to free memory.


## -parameters




### -param *








#### - memblock [in]

Previously allocated memory block to be freed.


## -returns



Deallocates a memory block (<i>memblock</i>) that was previously allocated by a call to a <a href="https://msdn.microsoft.com/f6a98721-ebd1-4d83-bc9d-adde2e3ce525">CFP_ALLOCPROC</a> or <a href="https://msdn.microsoft.com/06c45ea3-1776-4f9c-a931-461d0b697535">CFP_REALLOCPROC</a> callback function. If memblock is <b>NULL</b>, the pointer should be ignored and the function should return immediately. The function is not required to correctly handle being passed an invalid pointer (a pointer to a memory block that was not allocated by the appropriate <a href="https://msdn.microsoft.com/f6a98721-ebd1-4d83-bc9d-adde2e3ce525">CFP_ALLOCPROC</a> or <a href="https://msdn.microsoft.com/06c45ea3-1776-4f9c-a931-461d0b697535">CFP_REALLOCPROC</a> callback function).




## -remarks




<a href="74ded9cf-1863-432e-9306-327a42080bb8">free</a> conforms to this type; the application can either use <b>free</b> or a more specialized function. Whatever function is chosen, there must also be appropriate functions to allocate and to reallocate this memory. 
      




## -see-also




<a href="https://msdn.microsoft.com/f6a98721-ebd1-4d83-bc9d-adde2e3ce525">CFP_ALLOCPROC</a>



<a href="https://msdn.microsoft.com/06c45ea3-1776-4f9c-a931-461d0b697535">CFP_REALLOCPROC</a>



<a href="https://msdn.microsoft.com/aeea47c7-af55-46c4-b701-e00ec7540d24">CreateFontPackage</a>



<a href="https://msdn.microsoft.com/c51110a0-286c-4d97-9da5-4186ebf8f9b8">MergeFontPackage</a>
 

 

