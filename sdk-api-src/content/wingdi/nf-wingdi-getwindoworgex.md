---
UID: NF:wingdi.GetWindowOrgEx
title: GetWindowOrgEx function (wingdi.h)
description: The GetWindowOrgEx function retrieves the x-coordinates and y-coordinates of the window origin for the specified device context.
helpviewer_keywords: ["GetWindowOrgEx","GetWindowOrgEx function [Windows GDI]","_win32_GetWindowOrgEx","gdi.getwindoworgex","wingdi/GetWindowOrgEx"]
old-location: gdi\getwindoworgex.htm
tech.root: gdi
ms.assetid: 9579ed10-6d4c-4724-af8b-22cab5b6ff5e
ms.date: 12/05/2018
ms.keywords: GetWindowOrgEx, GetWindowOrgEx function [Windows GDI], _win32_GetWindowOrgEx, gdi.getwindoworgex, wingdi/GetWindowOrgEx
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
 - GetWindowOrgEx
 - wingdi/GetWindowOrgEx
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
 - GetWindowOrgEx
---

# GetWindowOrgEx function


## -description

The <b>GetWindowOrgEx</b> function retrieves the x-coordinates and y-coordinates of the window origin for the specified device context.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lppoint [out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that receives the coordinates, in logical units, of the window origin.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getviewportorgex">GetViewportOrgEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setviewportorgex">SetViewportOrgEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setwindoworgex">SetWindowOrgEx</a>