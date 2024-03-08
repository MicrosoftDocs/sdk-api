---
UID: NF:wingdi.GetRegionData
title: GetRegionData function (wingdi.h)
description: The GetRegionData function fills the specified buffer with data describing a region. This data includes the dimensions of the rectangles that make up the region.
helpviewer_keywords: ["GetRegionData","GetRegionData function [Windows GDI]","_win32_GetRegionData","gdi.getregiondata","wingdi/GetRegionData"]
old-location: gdi\getregiondata.htm
tech.root: gdi
ms.assetid: e0d4862d-a405-4c00-b7b0-af4dd60407c0
ms.date: 12/05/2018
ms.keywords: GetRegionData, GetRegionData function [Windows GDI], _win32_GetRegionData, gdi.getregiondata, wingdi/GetRegionData
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
 - GetRegionData
 - wingdi/GetRegionData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-rgn-l1-1-0.dll
 - Ext-MS-Win-RTCore-GDI-rgn-l1-1-0.dll
 - api-ms-win-gdi-ie-rgn-l1-1-0.dll
 - ie_shims.dll
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
 - GDI32Full.dll
api_name:
 - GetRegionData
---

## -description

The **GetRegionData** function fills the specified buffer with data describing a region. This data includes the dimensions of the rectangles that make up the region.

## -parameters

### -param hrgn [in]

A handle to the region.

### -param nCount [in]

The size, in bytes, of the *lpRgnData* buffer.

### -param lpRgnData [out]

A pointer to a [RGNDATA](/windows/win32/api/wingdi/ns-wingdi-rgndata) structure that receives the information. The dimensions of the region are in logical units. If this parameter is **NULL**, then the return value contains the number of bytes needed for the region data.

## -returns

If the function succeeds and *nCount* specifies an adequate number of bytes, then the return value equals the actual number of bytes used (less than or equal to *nCount*).

If *lpRgnData* is **NULL**, then the return value is the required number of bytes.

If the function fails, then the return value is zero.

If the failure is due to *hrgn* being invalid, then **GetLastError** returns **ERROR_INVALID_HANDLE**. Otherwise, **GetLastError** returns **ERROR_INVALID_PARAMETER** .

If *nCount* is too small, then the function fails.

## -remarks

The <b>GetRegionData</b> function is used in conjunction with the <a href="/windows/desktop/api/wingdi/nf-wingdi-extcreateregion">ExtCreateRegion</a> function.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createpolypolygonrgn">CreatePolyPolygonRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpolygonrgn">CreatePolygonRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgn">CreateRectRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgnindirect">CreateRectRgnIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createroundrectrgn">CreateRoundRectRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-extcreateregion">ExtCreateRegion</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-rgndata">RGNDATA</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>
