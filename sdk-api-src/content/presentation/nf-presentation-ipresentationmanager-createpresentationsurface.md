---
UID: NF:presentation.IPresentationManager.CreatePresentationSurface
tech.root: comp_swapchain
title: IPresentationManager::CreatePresentationSurface
ms.date: 06/08/2021
targetos: Windows
description: Creates a presentation surface for a piece of content that can be hosted in a visual tree and assigned a single front buffer.
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
 - IPresentationManager::CreatePresentationSurface
f1_keywords:
 - IPresentationManager::CreatePresentationSurface
 - presentation/IPresentationManager::CreatePresentationSurface
dev_langs:
 - c++
---

## -description

Creates a presentation surface for a piece of content that can be hosted in a visual tree and assigned a single front buffer.

## -parameters

### -param compositionSurfaceHandle

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**

A handle to the composition surface to bind the presentation surface to.

### -param presentationSurface

Type: **[IPresentationSurface](nn-presentation-ipresentationsurface.md)**

The created presentation surface.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

## -see-also

