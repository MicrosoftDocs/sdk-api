---
UID: NF:wingdi.ExtCreateRegion
title: ExtCreateRegion function (wingdi.h)
description: The ExtCreateRegion function creates a region from the specified region and transformation data.
helpviewer_keywords: ["ExtCreateRegion","ExtCreateRegion function [Windows GDI]","_win32_ExtCreateRegion","gdi.extcreateregion","wingdi/ExtCreateRegion"]
old-location: gdi\extcreateregion.htm
tech.root: gdi
ms.assetid: 4dcff824-eb1d-425c-b246-db4ace2c6518
ms.date: 12/05/2018
ms.keywords: ExtCreateRegion, ExtCreateRegion function [Windows GDI], _win32_ExtCreateRegion, gdi.extcreateregion, wingdi/ExtCreateRegion
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
 - ExtCreateRegion
 - wingdi/ExtCreateRegion
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
 - ExtCreateRegion
---

# ExtCreateRegion function


## -description

The <b>ExtCreateRegion</b> function creates a region from the specified region and transformation data.

## -parameters

### -param lpx [in]

A pointer to an <a href="/windows/desktop/api/wingdi/ns-wingdi-xform">XFORM</a> structure that defines the transformation to be performed on the region. If this pointer is <b>NULL</b>, the identity transformation is used.

### -param nCount [in]

The number of bytes pointed to by <i>lpRgnData</i>.

### -param lpData [in]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-rgndata">RGNDATA</a> structure that contains the region data in logical units.

## -returns

If the function succeeds, the return value is the value of the region.

If the function fails, the return value is <b>NULL</b>.

## -remarks

Region coordinates are represented as 27-bit signed integers.

An application can retrieve data for a region by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getregiondata">GetRegionData</a> function.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createpolypolygonrgn">CreatePolyPolygonRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpolygonrgn">CreatePolygonRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgn">CreateRectRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgnindirect">CreateRectRgnIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createroundrectrgn">CreateRoundRectRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getregiondata">GetRegionData</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-rgndata">RGNDATA</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-xform">XFORM</a>