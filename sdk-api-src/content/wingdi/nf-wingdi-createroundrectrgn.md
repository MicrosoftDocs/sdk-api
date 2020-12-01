---
UID: NF:wingdi.CreateRoundRectRgn
title: CreateRoundRectRgn function (wingdi.h)
description: The CreateRoundRectRgn function creates a rectangular region with rounded corners.
helpviewer_keywords: ["CreateRoundRectRgn","CreateRoundRectRgn function [Windows GDI]","_win32_CreateRoundRectRgn","gdi.createroundrectrgn","wingdi/CreateRoundRectRgn"]
old-location: gdi\createroundrectrgn.htm
tech.root: gdi
ms.assetid: 16f387e1-b00c-4755-8b21-1ee0f25bc46b
ms.date: 12/05/2018
ms.keywords: CreateRoundRectRgn, CreateRoundRectRgn function [Windows GDI], _win32_CreateRoundRectRgn, gdi.createroundrectrgn, wingdi/CreateRoundRectRgn
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
 - CreateRoundRectRgn
 - wingdi/CreateRoundRectRgn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
 - API-MS-Win-GDI-Internal-Uap-L1-1-0.dll
 - GDI32Full.dll
 - GDI32Min.dll
api_name:
 - CreateRoundRectRgn
---

# CreateRoundRectRgn function


## -description

The <b>CreateRoundRectRgn</b> function creates a rectangular region with rounded corners.

## -parameters

### -param x1 [in]

Specifies the x-coordinate of the upper-left corner of the region in device units.

### -param y1 [in]

Specifies the y-coordinate of the upper-left corner of the region in device units.

### -param x2 [in]

Specifies the x-coordinate of the lower-right corner of the region in device units.

### -param y2 [in]

Specifies the y-coordinate of the lower-right corner of the region in device units.

### -param w [in]

Specifies the width of the ellipse used to create the rounded corners in device units.

### -param h [in]

Specifies the height of the ellipse used to create the rounded corners in device units.

## -returns

If the function succeeds, the return value is the handle to the region.

If the function fails, the return value is <b>NULL</b>.

## -remarks

When you no longer need the <b>HRGN</b> object call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

Region coordinates are represented as 27-bit signed  integers.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createpolypolygonrgn">CreatePolyPolygonRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpolygonrgn">CreatePolygonRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgn">CreateRectRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgnindirect">CreateRectRgnIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-extcreateregion">ExtCreateRegion</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getregiondata">GetRegionData</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>