---
UID: NC:fontsub.CFP_FREEPROC
title: CFP_FREEPROC
author: windows-sdk-content
description: Client-provided callback function, used by CreateFontPackage and MergeFontPackage to free memory.
old-location: gdi\cfp_freeproc.htm
tech.root: gdi
ms.assetid: cd99e704-b3a8-4d55-946f-76dd47b2a030
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CFP_FREEPROC, CFP_FREEPROC callback, CFP_FREEPROC callback function [Windows GDI], _win32_CFP_FREEPROC, fontsub/CFP_FREEPROC, gdi.cfp_freeproc
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
 - CFP_FREEPROC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Dd318652(v=VS.85).aspx">free</a> conforms to this type; the application can either use <b>free</b> or a more specialized function. Whatever function is chosen, there must also be appropriate functions to allocate and to reallocate this memory. 
      




## -see-also




<a href="https://msdn.microsoft.com/f6a98721-ebd1-4d83-bc9d-adde2e3ce525">CFP_ALLOCPROC</a>



<a href="https://msdn.microsoft.com/06c45ea3-1776-4f9c-a931-461d0b697535">CFP_REALLOCPROC</a>



<a href="https://msdn.microsoft.com/aeea47c7-af55-46c4-b701-e00ec7540d24">CreateFontPackage</a>



<a href="https://msdn.microsoft.com/c51110a0-286c-4d97-9da5-4186ebf8f9b8">MergeFontPackage</a>
 

 

