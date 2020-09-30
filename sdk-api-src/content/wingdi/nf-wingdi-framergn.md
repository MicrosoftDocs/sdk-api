---
UID: NF:wingdi.FrameRgn
title: FrameRgn function (wingdi.h)
description: The FrameRgn function draws a border around the specified region by using the specified brush.
helpviewer_keywords: ["FrameRgn","FrameRgn function [Windows GDI]","_win32_FrameRgn","gdi.framergn","wingdi/FrameRgn"]
old-location: gdi\framergn.htm
tech.root: gdi
ms.assetid: d2c95392-7950-4963-8f10-2387daf23e93
ms.date: 12/05/2018
ms.keywords: FrameRgn, FrameRgn function [Windows GDI], _win32_FrameRgn, gdi.framergn, wingdi/FrameRgn
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
 - FrameRgn
 - wingdi/FrameRgn
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
 - FrameRgn
---

# FrameRgn function


## -description

The <b>FrameRgn</b> function draws a border around the specified region by using the specified brush.

## -parameters

### -param hdc [in]

Handle to the device context.

### -param hrgn [in]

Handle to the region to be enclosed in a border. The region's coordinates are presumed to be in logical units.

### -param hbr [in]

Handle to the brush to be used to draw the border.

### -param w [in]

Specifies the width, in logical units, of vertical brush strokes.

### -param h [in]

Specifies the height, in logical units, of horizontal brush strokes.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-fillrgn">FillRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-paintrgn">PaintRgn</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>