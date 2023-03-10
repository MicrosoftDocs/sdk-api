---
UID: NF:wingdi.InvertRgn
title: InvertRgn function (wingdi.h)
description: The InvertRgn function inverts the colors in the specified region.
helpviewer_keywords: ["InvertRgn","InvertRgn function [Windows GDI]","_win32_InvertRgn","gdi.invertrgn","wingdi/InvertRgn"]
old-location: gdi\invertrgn.htm
tech.root: gdi
ms.assetid: 94704c44-796a-4ca7-97f3-6676d7f94078
ms.date: 12/05/2018
ms.keywords: InvertRgn, InvertRgn function [Windows GDI], _win32_InvertRgn, gdi.invertrgn, wingdi/InvertRgn
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
 - InvertRgn
 - wingdi/InvertRgn
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
 - InvertRgn
---

# InvertRgn function


## -description

The <b>InvertRgn</b> function inverts the colors in the specified region.

## -parameters

### -param hdc [in]

Handle to the device context.

### -param hrgn [in]

Handle to the region for which colors are inverted. The region's coordinates are presumed to be logical coordinates.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

On monochrome screens, the <b>InvertRgn</b> function makes white pixels black and black pixels white. On color screens, this inversion is dependent on the type of technology used to generate the colors for the screen.


#### Examples

For an example, see <a href="/windows/desktop/gdi/using-brushes">Using Brushes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-fillrgn">FillRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-paintrgn">PaintRgn</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>