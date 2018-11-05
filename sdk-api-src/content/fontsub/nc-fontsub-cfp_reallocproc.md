---
UID: NC:fontsub.CFP_REALLOCPROC
title: CFP_REALLOCPROC
author: windows-sdk-content
description: Client-provided callback function, used by CreateFontPackage and MergeFontPackage to reallocate memory when the size of an allocated buffer needs to change.
old-location: gdi\cfp_reallocproc.htm
tech.root: gdi
ms.assetid: 06c45ea3-1776-4f9c-a931-461d0b697535
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CFP_REALLOCPROC, CFP_REALLOCPROC callback, CFP_REALLOCPROC callback function [Windows GDI], _win32_CFP_REALLOCPROC, fontsub/CFP_REALLOCPROC, gdi.cfp_reallocproc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: fontsub.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - FontSub.h
api_name:
 - CFP_REALLOCPROC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="2b2239de-810b-4b11-9438-32ab0a244185">realloc</a>conforms to this type; the application can either use <b>realloc</b> or a more specialized function for memory reallocation. Whatever function is chosen, there must also be appropriate functions for initial allocation and to free this memory.




## -see-also




<a href="https://msdn.microsoft.com/f6a98721-ebd1-4d83-bc9d-adde2e3ce525">CFP_ALLOCPROC</a>



<a href="https://msdn.microsoft.com/cd99e704-b3a8-4d55-946f-76dd47b2a030">CFP_FREEPROC</a>



<a href="https://msdn.microsoft.com/aeea47c7-af55-46c4-b701-e00ec7540d24">CreateFontPackage</a>



<a href="https://msdn.microsoft.com/c51110a0-286c-4d97-9da5-4186ebf8f9b8">MergeFontPackage</a>
 

 

