---
UID: NC:fontsub.CFP_REALLOCPROC
title: CFP_REALLOCPROC (fontsub.h)
description: Client-provided callback function, used by CreateFontPackage and MergeFontPackage to reallocate memory when the size of an allocated buffer needs to change.
helpviewer_keywords: ["CFP_REALLOCPROC","CFP_REALLOCPROC callback","CFP_REALLOCPROC callback function [Windows GDI]","_win32_CFP_REALLOCPROC","fontsub/CFP_REALLOCPROC","gdi.cfp_reallocproc"]
old-location: gdi\cfp_reallocproc.htm
tech.root: gdi
ms.assetid: 06c45ea3-1776-4f9c-a931-461d0b697535
ms.date: 12/05/2018
ms.keywords: CFP_REALLOCPROC, CFP_REALLOCPROC callback, CFP_REALLOCPROC callback function [Windows GDI], _win32_CFP_REALLOCPROC, fontsub/CFP_REALLOCPROC, gdi.cfp_reallocproc
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
 - CFP_REALLOCPROC
 - fontsub/CFP_REALLOCPROC
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
 - CFP_REALLOCPROC
---

## -description

Client-provided callback function, used by <a href="/windows/desktop/api/fontsub/nf-fontsub-createfontpackage">CreateFontPackage</a> and <a href="/windows/desktop/api/fontsub/nf-fontsub-mergefontpackage">MergeFontPackage</a> to reallocate memory when the size of an allocated buffer needs to change.

## -parameters

### -param unnamedParam1

Pointer to previously allocated memory block.

### -param unnamedParam2

New size in bytes.

## -returns

Returns a void pointer to the reallocated (and possibly moved) memory block. The return value should be <b>NULL</b> if the size is zero and the <i>memblock</i> argument is not <b>NULL</b>, or if there is not enough available memory to expand the block to the given size. In the first case, the original block should be freed. In the second, the original block should be unchanged.

## -remarks

<a href="/previous-versions/visualstudio/visual-studio-2010/xbebcx7d(v=vs.100)">realloc</a> conforms to this type; the application can either use <b>realloc</b> or a more specialized function for memory reallocation. Whatever function is chosen, there must also be appropriate functions for initial allocation and to free this memory.

## -see-also

<a href="/windows/desktop/api/fontsub/nc-fontsub-cfp_allocproc">CFP_ALLOCPROC</a>



<a href="/windows/desktop/api/fontsub/nc-fontsub-cfp_freeproc">CFP_FREEPROC</a>



<a href="/windows/desktop/api/fontsub/nf-fontsub-createfontpackage">CreateFontPackage</a>



<a href="/windows/desktop/api/fontsub/nf-fontsub-mergefontpackage">MergeFontPackage</a>
