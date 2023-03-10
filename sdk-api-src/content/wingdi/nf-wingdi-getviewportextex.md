---
UID: NF:wingdi.GetViewportExtEx
title: GetViewportExtEx function (wingdi.h)
description: The GetViewportExtEx function retrieves the x-extent and y-extent of the current viewport for the specified device context.
helpviewer_keywords: ["GetViewportExtEx","GetViewportExtEx function [Windows GDI]","_win32_GetViewportExtEx","gdi.getviewportextex","wingdi/GetViewportExtEx"]
old-location: gdi\getviewportextex.htm
tech.root: gdi
ms.assetid: e3fc188a-3796-497d-9d86-f116e9e48e30
ms.date: 12/05/2018
ms.keywords: GetViewportExtEx, GetViewportExtEx function [Windows GDI], _win32_GetViewportExtEx, gdi.getviewportextex, wingdi/GetViewportExtEx
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetViewportExtEx
 - wingdi/GetViewportExtEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetViewportExtEx
---

# GetViewportExtEx function


## -description

The <b>GetViewportExtEx</b> function retrieves the x-extent and y-extent of the current viewport for the specified device context.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lpsize [out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure that receives the x- and y-extents, in device units.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getwindowextex">GetWindowExtEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setviewportextex">SetViewportExtEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setwindowextex">SetWindowExtEx</a>