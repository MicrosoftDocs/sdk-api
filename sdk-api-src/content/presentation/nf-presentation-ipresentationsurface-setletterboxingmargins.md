---
UID: NF:presentation.IPresentationSurface.SetLetterboxingMargins
tech.root: comp_swapchain
title: IPresentationSurface::SetLetterboxingMargins
ms.date: 06/08/2021
targetos: Windows
description: Sets the size, in visual space, taken by each letterbox area.
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
 - IPresentationSurface::SetLetterboxingMargins
f1_keywords:
 - IPresentationSurface::SetLetterboxingMargins
 - presentation/IPresentationSurface::SetLetterboxingMargins
dev_langs:
 - c++
---

## -description

Sets the size, in visual space, taken by each letterbox area.

## -parameters

### -param leftLetterboxSize

Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**

The size of the left margin of the letterbox area.

### -param topLetterboxSize

Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**

The size of the top margin of the letterbox area.

### -param rightLetterboxSize

Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**

The size of the right margin of the letterbox area.

### -param bottomLetterboxSize

Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**

The size of the bottom margin of the letterbox area.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

Margins are not affected by the scale component of the transform, but are affected by every other component. Put another way, the margins are applied with the transform applied, but compensate their own size by any scale present in that transform.

## -see-also

