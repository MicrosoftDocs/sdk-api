---
UID: NF:wingdi.StrokeAndFillPath
title: StrokeAndFillPath function (wingdi.h)
description: The StrokeAndFillPath function closes any open figures in a path, strokes the outline of the path by using the current pen, and fills its interior by using the current brush.
helpviewer_keywords: ["StrokeAndFillPath","StrokeAndFillPath function [Windows GDI]","_win32_StrokeAndFillPath","gdi.strokeandfillpath","wingdi/StrokeAndFillPath"]
old-location: gdi\strokeandfillpath.htm
tech.root: gdi
ms.assetid: 936af9e5-707d-4d43-9035-e8239e3759a2
ms.date: 12/05/2018
ms.keywords: StrokeAndFillPath, StrokeAndFillPath function [Windows GDI], _win32_StrokeAndFillPath, gdi.strokeandfillpath, wingdi/StrokeAndFillPath
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
 - StrokeAndFillPath
 - wingdi/StrokeAndFillPath
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
 - StrokeAndFillPath
---

# StrokeAndFillPath function


## -description

The <b>StrokeAndFillPath</b> function closes any open figures in a path, strokes the outline of the path by using the current pen, and fills its interior by using the current brush.

## -parameters

### -param hdc [in]

A handle to the device context.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The device context identified by the <i>hdc</i> parameter must contain a closed path.

The <b>StrokeAndFillPath</b> function has the same effect as closing all the open figures in the path, and stroking and filling the path separately, except that the filled region will not overlap the stroked region even if the pen is wide.


#### Examples

For an example, see <a href="/windows/desktop/gdi/drawing-a-pie-chart">Drawing a Pie Chart</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-beginpath">BeginPath</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-fillpath">FillPath</a>



<a href="/windows/desktop/gdi/path-functions">Path Functions</a>



<a href="/windows/desktop/gdi/paths">Paths Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setpolyfillmode">SetPolyFillMode</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-strokepath">StrokePath</a>