---
UID: NF:wingdi.RectInRegion
title: RectInRegion function (wingdi.h)
description: The RectInRegion function determines whether any part of the specified rectangle is within the boundaries of a region.
helpviewer_keywords: ["RectInRegion","RectInRegion function [Windows GDI]","_win32_RectInRegion","gdi.rectinregion","wingdi/RectInRegion"]
old-location: gdi\rectinregion.htm
tech.root: gdi
ms.assetid: 198a02f1-120c-4f65-aa7c-a41f2e5e81a9
ms.date: 12/05/2018
ms.keywords: RectInRegion, RectInRegion function [Windows GDI], _win32_RectInRegion, gdi.rectinregion, wingdi/RectInRegion
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
 - RectInRegion
 - wingdi/RectInRegion
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
 - RectInRegion
---

# RectInRegion function


## -description

The <b>RectInRegion</b> function determines whether any part of the specified rectangle is within the boundaries of a region.

## -parameters

### -param hrgn [in]

Handle to the region.

### -param lprect [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the coordinates of the rectangle in logical units. The lower and right edges of the rectangle are not included.

## -returns

If any part of the specified rectangle lies within the boundaries of the region, the return value is nonzero.

If no part of the specified rectangle lies within the boundaries of the region, the return value is zero.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-ptinregion">PtInRegion</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>