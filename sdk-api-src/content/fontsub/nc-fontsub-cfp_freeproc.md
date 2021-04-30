---
UID: NC:fontsub.CFP_FREEPROC
title: CFP_FREEPROC (fontsub.h)
description: Client-provided callback function, used by CreateFontPackage and MergeFontPackage to free memory.
helpviewer_keywords: ["CFP_FREEPROC","CFP_FREEPROC callback","CFP_FREEPROC callback function [Windows GDI]","_win32_CFP_FREEPROC","fontsub/CFP_FREEPROC","gdi.cfp_freeproc"]
old-location: gdi\cfp_freeproc.htm
tech.root: gdi
ms.assetid: cd99e704-b3a8-4d55-946f-76dd47b2a030
ms.date: 12/05/2018
ms.keywords: CFP_FREEPROC, CFP_FREEPROC callback, CFP_FREEPROC callback function [Windows GDI], _win32_CFP_FREEPROC, fontsub/CFP_FREEPROC, gdi.cfp_freeproc
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CFP_FREEPROC
 - fontsub/CFP_FREEPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - FontSub.h
api_name:
 - CFP_FREEPROC
---

## -description

Client-provided callback function, used by <a href="/windows/desktop/api/fontsub/nf-fontsub-createfontpackage">CreateFontPackage</a> and <a href="/windows/desktop/api/fontsub/nf-fontsub-mergefontpackage">MergeFontPackage</a> to free memory.

## -parameters

### -param unnamedParam1

Previously allocated memory block to be freed.

## -returns

Deallocates a memory block (<i>memblock</i>) that was previously allocated by a call to a <a href="/windows/desktop/api/fontsub/nc-fontsub-cfp_allocproc">CFP_ALLOCPROC</a> or <a href="/windows/desktop/api/fontsub/nc-fontsub-cfp_reallocproc">CFP_REALLOCPROC</a> callback function. If memblock is <b>NULL</b>, the pointer should be ignored and the function should return immediately. The function is not required to correctly handle being passed an invalid pointer (a pointer to a memory block that was not allocated by the appropriate <a href="/windows/desktop/api/fontsub/nc-fontsub-cfp_allocproc">CFP_ALLOCPROC</a> or <a href="/windows/desktop/api/fontsub/nc-fontsub-cfp_reallocproc">CFP_REALLOCPROC</a> callback function).

## -remarks

<a href="/windows/desktop/DirectShow/cbaseallocator-free">free</a> conforms to this type; the application can either use <b>free</b> or a more specialized function. Whatever function is chosen, there must also be appropriate functions to allocate and to reallocate this memory.

## -see-also

<a href="/windows/desktop/api/fontsub/nc-fontsub-cfp_allocproc">CFP_ALLOCPROC</a>



<a href="/windows/desktop/api/fontsub/nc-fontsub-cfp_reallocproc">CFP_REALLOCPROC</a>



<a href="/windows/desktop/api/fontsub/nf-fontsub-createfontpackage">CreateFontPackage</a>



<a href="/windows/desktop/api/fontsub/nf-fontsub-mergefontpackage">MergeFontPackage</a>
