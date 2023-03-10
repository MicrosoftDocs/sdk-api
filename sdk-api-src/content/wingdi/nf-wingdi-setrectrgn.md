---
UID: NF:wingdi.SetRectRgn
title: SetRectRgn function (wingdi.h)
description: The SetRectRgn function converts a region into a rectangular region with the specified coordinates.
helpviewer_keywords: ["SetRectRgn","SetRectRgn function [Windows GDI]","_win32_SetRectRgn","gdi.setrectrgn","wingdi/SetRectRgn"]
old-location: gdi\setrectrgn.htm
tech.root: gdi
ms.assetid: 9a024d61-f397-43d8-a48e-edb8102a6f55
ms.date: 12/05/2018
ms.keywords: SetRectRgn, SetRectRgn function [Windows GDI], _win32_SetRectRgn, gdi.setrectrgn, wingdi/SetRectRgn
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
 - SetRectRgn
 - wingdi/SetRectRgn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-RTCore-GDI-rgn-l1-1-0.dll
 - api-ms-win-gdi-ie-rgn-l1-1-0.dll
 - ie_shims.dll
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
api_name:
 - SetRectRgn
---

# SetRectRgn function


## -description

The <b>SetRectRgn</b> function converts a region into a rectangular region with the specified coordinates.

## -parameters

### -param hrgn [in]

Handle to the region.

### -param left [in]

Specifies the x-coordinate of the upper-left corner of the rectangular region in logical units.

### -param top [in]

Specifies the y-coordinate of the upper-left corner of the rectangular region in logical units.

### -param right [in]

Specifies the x-coordinate of the lower-right corner of the rectangular region in logical units.

### -param bottom [in]

Specifies the y-coordinate of the lower-right corner of the rectangular region in logical units.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The region does not include the lower and right boundaries of the rectangle.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgn">CreateRectRgn</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>