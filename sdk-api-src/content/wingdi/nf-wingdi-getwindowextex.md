---
UID: NF:wingdi.GetWindowExtEx
title: GetWindowExtEx function (wingdi.h)
description: This function retrieves the x-extent and y-extent of the window for the specified device context.
helpviewer_keywords: ["GetWindowExtEx","GetWindowExtEx function [Windows GDI]","_win32_GetWindowExtEx","gdi.getwindowextex","wingdi/GetWindowExtEx"]
old-location: gdi\getwindowextex.htm
tech.root: gdi
ms.assetid: 17f41fcb-c9a4-4b7e-acde-73450044413e
ms.date: 12/05/2018
ms.keywords: GetWindowExtEx, GetWindowExtEx function [Windows GDI], _win32_GetWindowExtEx, gdi.getwindowextex, wingdi/GetWindowExtEx
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
 - GetWindowExtEx
 - wingdi/GetWindowExtEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-L1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetWindowExtEx
---

# GetWindowExtEx function


## -description

This function retrieves the x-extent and y-extent of the window for the specified device context.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lpsize [out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure that receives the x- and y-extents in page-space units, that is, logical units.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getviewportextex">GetViewportExtEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setviewportextex">SetViewportExtEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setwindowextex">SetWindowExtEx</a>