---
UID: NF:wingdi.FillRgn
title: FillRgn function (wingdi.h)
description: The FillRgn function fills a region by using the specified brush.
helpviewer_keywords: ["FillRgn","FillRgn function [Windows GDI]","_win32_FillRgn","gdi.fillrgn","wingdi/FillRgn"]
old-location: gdi\fillrgn.htm
tech.root: gdi
ms.assetid: c4e0eca5-442b-462b-a4f2-0c628b6d3d38
ms.date: 12/05/2018
ms.keywords: FillRgn, FillRgn function [Windows GDI], _win32_FillRgn, gdi.fillrgn, wingdi/FillRgn
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
 - FillRgn
 - wingdi/FillRgn
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
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
 - API-MS-Win-GDI-Internal-Uap-L1-1-0.dll
 - GDI32Full.dll
 - GDI32Min.dll
api_name:
 - FillRgn
---

# FillRgn function


## -description

The <b>FillRgn</b> function fills a region by using the specified brush.

## -parameters

### -param hdc [in]

Handle to the device context.

### -param hrgn [in]

Handle to the region to be filled. The region's coordinates are presumed to be in logical units.

### -param hbr [in]

Handle to the brush to be used to fill the region.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect">CreateBrushIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrush">CreateDIBPatternBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createhatchbrush">CreateHatchBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpatternbrush">CreatePatternBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush">CreateSolidBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-paintrgn">PaintRgn</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>