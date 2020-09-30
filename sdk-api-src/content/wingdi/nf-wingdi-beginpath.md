---
UID: NF:wingdi.BeginPath
title: BeginPath function (wingdi.h)
description: The BeginPath function opens a path bracket in the specified device context.
helpviewer_keywords: ["BeginPath","BeginPath function [Windows GDI]","_win32_BeginPath","gdi.beginpath","wingdi/BeginPath"]
old-location: gdi\beginpath.htm
tech.root: gdi
ms.assetid: 88be3405-a420-4eb1-935b-099dc3067530
ms.date: 12/05/2018
ms.keywords: BeginPath, BeginPath function [Windows GDI], _win32_BeginPath, gdi.beginpath, wingdi/BeginPath
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
 - BeginPath
 - wingdi/BeginPath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Path-l1-1-0.dll
 - GDI32Full.dll
api_name:
 - BeginPath
---

# BeginPath function


## -description

The <b>BeginPath</b> function opens a path bracket in the specified device context.

## -parameters

### -param hdc [in]

A handle to the device context.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

After a path bracket is open, an application can begin calling GDI drawing functions to define the points that lie in the path. An application can close an open path bracket by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-endpath">EndPath</a> function.

When an application calls <b>BeginPath</b> for a device context, any previous paths are discarded from that device context. The following list shows which drawing functions can be used.

<ul>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-anglearc">AngleArc</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-arc">Arc</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-arcto">ArcTo</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-chord">Chord</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-closefigure">CloseFigure</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-ellipse">Ellipse</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-lineto">LineTo</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-movetoex">MoveToEx</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-pie">Pie</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-polybezier">PolyBezier</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-polybezierto">PolyBezierTo</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-polydraw">PolyDraw</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-polygon">Polygon</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-polyline">Polyline</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-polylineto">PolylineTo</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-polypolygon">PolyPolygon</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-polypolyline">PolyPolyline</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-rectangle">Rectangle</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-roundrect">RoundRect</a>
</li>
<li>
<a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a>
</li>
</ul>

#### Examples

For an example, see <a href="/windows/desktop/gdi/using-paths">Using Paths</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-endpath">EndPath</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-fillpath">FillPath</a>



<a href="/windows/desktop/gdi/path-functions">Path Functions</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-pathtoregion">PathToRegion</a>



<a href="/windows/desktop/gdi/paths">Paths Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectclippath">SelectClipPath</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-strokeandfillpath">StrokeAndFillPath</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-strokepath">StrokePath</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-widenpath">WidenPath</a>