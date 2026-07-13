---
UID: NF:presentation.IPresentationSurface.SetBuffer
tech.root: comp_swapchain
title: IPresentationSurface::SetBuffer
ms.date: 06/08/2021
targetos: Windows
description: Sets the presentation buffer associated with this presentation surface.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: dcomp.dll
req.header: presentation.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: dcomp.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - presentation.h
api_name:
 - IPresentationSurface::SetBuffer
f1_keywords:
 - IPresentationSurface::SetBuffer
 - presentation/IPresentationSurface::SetBuffer
dev_langs:
 - c++
---

## -description

Sets the presentation buffer associated with this presentation surface.

## -parameters

### -param presentationBuffer

Type: **[IPresentationBuffer](nn-presentation-ipresentationbuffer.md)**

The presentation buffer associated with this presentation surface.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

## -see-also

