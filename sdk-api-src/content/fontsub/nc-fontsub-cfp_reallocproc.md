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

# CFP_REALLOCPROC callback function


## -description



          
        Client-provided callback function, used by <a href="https://msdn.microsoft.com/aeea47c7-af55-46c4-b701-e00ec7540d24">CreateFontPackage</a> and <a href="https://msdn.microsoft.com/c51110a0-286c-4d97-9da5-4186ebf8f9b8">MergeFontPackage</a> to reallocate memory when the size of an allocated buffer needs to change.


## -parameters




### -param *


### -param Arg1








#### - memblock [in]

Pointer to previously allocated memory block.


#### - size [in]

New size in bytes.


## -returns



Returns a void pointer to the reallocated (and possibly moved) memory block. The return value should be <b>NULL</b> if the size is zero and the <i>memblock</i> argument is not <b>NULL</b>, or if there is not enough available memory to expand the block to the given size. In the first case, the original block should be freed. In the second, the original block should be unchanged.




## -remarks




<a href="2b2239de-810b-4b11-9438-32ab0a244185">realloc</a>
      conforms to this type; the application can either use <b>realloc</b> or a more specialized function for memory reallocation. Whatever function is chosen, there must also be appropriate functions for initial allocation and to free this memory.




## -see-also




<a href="https://msdn.microsoft.com/f6a98721-ebd1-4d83-bc9d-adde2e3ce525">CFP_ALLOCPROC</a>



<a href="https://msdn.microsoft.com/cd99e704-b3a8-4d55-946f-76dd47b2a030">CFP_FREEPROC</a>



<a href="https://msdn.microsoft.com/aeea47c7-af55-46c4-b701-e00ec7540d24">CreateFontPackage</a>



<a href="https://msdn.microsoft.com/c51110a0-286c-4d97-9da5-4186ebf8f9b8">MergeFontPackage</a>
 

 

