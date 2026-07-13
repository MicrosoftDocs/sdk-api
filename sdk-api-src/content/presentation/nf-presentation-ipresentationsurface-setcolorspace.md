---
UID: NF:presentation.IPresentationSurface.SetColorSpace
tech.root: comp_swapchain
title: IPresentationSurface::SetColorSpace
ms.date: 06/08/2021
targetos: Windows
description: Sets the type of color space used by the presentation surface.
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
 - IPresentationSurface::SetColorSpace
f1_keywords:
 - IPresentationSurface::SetColorSpace
 - presentation/IPresentationSurface::SetColorSpace
dev_langs:
 - c++
---

## -description

Sets the type of color space used by the presentation surface.

## -parameters

### -param colorSpace

Type: **[DXGI_COLOR_SPACE_TYPE](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)**

The type of color space used by the presentation surface.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

## -see-also

