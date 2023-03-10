---
UID: NF:wingdi.PaintRgn
title: PaintRgn function (wingdi.h)
description: The PaintRgn function paints the specified region by using the brush currently selected into the device context.
helpviewer_keywords: ["PaintRgn","PaintRgn function [Windows GDI]","_win32_PaintRgn","gdi.paintrgn","wingdi/PaintRgn"]
old-location: gdi\paintrgn.htm
tech.root: gdi
ms.assetid: 7656fb67-d865-459e-b379-4f2e44c76fd0
ms.date: 12/05/2018
ms.keywords: PaintRgn, PaintRgn function [Windows GDI], _win32_PaintRgn, gdi.paintrgn, wingdi/PaintRgn
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
 - PaintRgn
 - wingdi/PaintRgn
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
 - PaintRgn
---

# PaintRgn function


## -description

The <b>PaintRgn</b> function paints the specified region by using the brush currently selected into the device context.

## -parameters

### -param hdc [in]

Handle to the device context.

### -param hrgn [in]

Handle to the region to be filled. The region's coordinates are presumed to be logical coordinates.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-fillrgn">FillRgn</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>