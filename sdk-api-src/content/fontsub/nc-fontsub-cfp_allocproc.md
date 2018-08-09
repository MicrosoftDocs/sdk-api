---
UID: NC:fontsub.CFP_ALLOCPROC
title: CFP_ALLOCPROC
author: windows-sdk-content
description: Client-provided callback function, used by CreateFontPackage and MergeFontPackage to allocate memory.
old-location: gdi\cfp_allocproc.htm
old-project: gdi
ms.assetid: f6a98721-ebd1-4d83-bc9d-adde2e3ce525
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CFP_ALLOCPROC, CFP_ALLOCPROC callback, CFP_ALLOCPROC callback function [Windows GDI], _win32_CFP_ALLOCPROC, fontsub/CFP_ALLOCPROC, gdi.cfp_allocproc
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
tech.root: 
req.typenames: FILTERED_DATA_SOURCES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - FontSub.h
api_name:
 - CFP_ALLOCPROC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# CFP_ALLOCPROC callback function


## -description


Client-provided callback function, used by <a href="https://msdn.microsoft.com/aeea47c7-af55-46c4-b701-e00ec7540d24">CreateFontPackage</a> and <a href="https://msdn.microsoft.com/c51110a0-286c-4d97-9da5-4186ebf8f9b8">MergeFontPackage</a> to allocate memory.
          
        


## -parameters




### -param Arg1








#### - size [in]

Number of bytes to allocate.


## -returns



Returns a void pointer to the allocated space, or <b>NULL</b> if there is insufficient memory available.




## -remarks




<a href="144fcee2-be34-4a03-bb7e-ed6d4b99eea0">malloc</a> conforms to this type; the application can either use <b>malloc</b> or a more specialized function for memory allocation. Whatever function is chosen, there must also be appropriate functions to reallocate and to free this memory. 




## -see-also




<a href="https://msdn.microsoft.com/cd99e704-b3a8-4d55-946f-76dd47b2a030">CFP_FREEPROC</a>



<a href="https://msdn.microsoft.com/06c45ea3-1776-4f9c-a931-461d0b697535">CFP_REALLOCPROC</a>



<a href="https://msdn.microsoft.com/aeea47c7-af55-46c4-b701-e00ec7540d24">CreateFontPackage</a>



<a href="https://msdn.microsoft.com/c51110a0-286c-4d97-9da5-4186ebf8f9b8">MergeFontPackage</a>
 

 

