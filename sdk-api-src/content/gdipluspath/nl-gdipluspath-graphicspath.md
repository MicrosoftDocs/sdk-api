---
UID: NL:gdipluspath.GraphicsPath
title: GraphicsPath (gdipluspath.h)
description: A GraphicsPath object stores a sequence of lines, curves, and shapes.
helpviewer_keywords: ["GraphicsPath","GraphicsPath class [GDI+]","GraphicsPath class [GDI+]","described","_gdiplus_CLASS_GraphicsPath_Class","gdiplus._gdiplus_CLASS_GraphicsPath_Class","gdipluspath/GraphicsPath"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspath.htm
ms.date: 12/05/2018
ms.keywords: GraphicsPath, GraphicsPath class [GDI+], GraphicsPath class [GDI+],described, _gdiplus_CLASS_GraphicsPath_Class, gdiplus._gdiplus_CLASS_GraphicsPath_Class, gdipluspath/GraphicsPath
req.header: gdipluspath.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GraphicsPath
 - gdipluspath/GraphicsPath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPath
---

# GraphicsPath class


## -description

A <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-graphicspath(constgraphicspath_)">GraphicsPath</a> object stores a sequence of lines, curves, and shapes. You can draw the entire sequence by calling the 
			<b>DrawPath</b> method of a 
			<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. You can partition the sequence of lines, curves, and shapes into figures, and with the help of a 
			<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a> object, you can draw selected figures. You can also place markers in the sequence, so that you can draw selected portions of the path.

## -remarks

A path consists of one or more figures. As you add lines and curves to a path, those lines and curves become part of a figure. You can start a new figure by calling the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-startfigure">GraphicsPath::StartFigure</a> method. When you draw a path, the lines and curves within an individual figure are connected by straight lines; the ending point of one line or curve is connected to the starting point of the next line or curve. No connecting line is drawn between the end of one figure and the start of the next figure.

A figure can be open or closed. You can close a figure by calling the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-closefigure">GraphicsPath::CloseFigure</a> method. After you call <b>GraphicsPath::CloseFigure</b>, the next line, curve, or shape that you add to the path is part of the next figure. When you draw a path, the ending point of each closed figure is automatically connected to the starting point of that figure.

Some shapes (for example, rectangles and ellipses) are intrinsically closed. When you add an intrinsically closed shape to a path, that shape is in a figure by itself, and that figure is considered closed even if you don't call <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-closefigure">GraphicsPath::CloseFigure</a>. The following methods add intrinsically closed figures to a path: 

<ul>
<li>
<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint_inreal)">AddClosedCurve Methods</a>
</li>
<li>
<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inconstrect_)">AddEllipse Methods</a>
</li>
<li>
<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addpie(inconstrect__inreal_inreal)">AddPie Methods</a>
</li>
<li>
<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpoint_inint)">AddPolygon Methods</a>
</li>
<li>
<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrect_)">AddRectangle Methods</a>
</li>
<li>
<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrect_int)">AddRectangles Methods</a>
</li>
<li>
<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addstring(inconstwchar_inint_inconstfontfamily_inint_inreal_inconstpoint__inconststringformat)">AddString Methods</a>
</li>
</ul>