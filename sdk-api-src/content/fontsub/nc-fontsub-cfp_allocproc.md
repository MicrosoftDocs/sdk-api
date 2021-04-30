---
UID: NC:fontsub.CFP_ALLOCPROC
title: CFP_ALLOCPROC (fontsub.h)
description: Client-provided callback function, used by CreateFontPackage and MergeFontPackage to allocate memory.
helpviewer_keywords: ["CFP_ALLOCPROC","CFP_ALLOCPROC callback","CFP_ALLOCPROC callback function [Windows GDI]","_win32_CFP_ALLOCPROC","fontsub/CFP_ALLOCPROC","gdi.cfp_allocproc"]
old-location: gdi\cfp_allocproc.htm
tech.root: gdi
ms.assetid: f6a98721-ebd1-4d83-bc9d-adde2e3ce525
ms.date: 12/05/2018
ms.keywords: CFP_ALLOCPROC, CFP_ALLOCPROC callback, CFP_ALLOCPROC callback function [Windows GDI], _win32_CFP_ALLOCPROC, fontsub/CFP_ALLOCPROC, gdi.cfp_allocproc
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
 - CFP_ALLOCPROC
 - fontsub/CFP_ALLOCPROC
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
 - CFP_ALLOCPROC
---

## -description

Client-provided callback function, used by <a href="/windows/desktop/api/fontsub/nf-fontsub-createfontpackage">CreateFontPackage</a> and <a href="/windows/desktop/api/fontsub/nf-fontsub-mergefontpackage">MergeFontPackage</a> to allocate memory.

## -parameters

### -param unnamedParam1

Number of bytes to allocate.

## -returns

Returns a void pointer to the allocated space, or <b>NULL</b> if there is insufficient memory available.

## -remarks

<a href="/previous-versions/visualstudio/visual-studio-2010/6ewkz86d(v=vs.100)">malloc</a> conforms to this type; the application can either use <b>malloc</b> or a more specialized function for memory allocation. Whatever function is chosen, there must also be appropriate functions to reallocate and to free this memory.

## -see-also

<a href="/windows/desktop/api/fontsub/nc-fontsub-cfp_freeproc">CFP_FREEPROC</a>



<a href="/windows/desktop/api/fontsub/nc-fontsub-cfp_reallocproc">CFP_REALLOCPROC</a>



<a href="/windows/desktop/api/fontsub/nf-fontsub-createfontpackage">CreateFontPackage</a>



<a href="/windows/desktop/api/fontsub/nf-fontsub-mergefontpackage">MergeFontPackage</a>
