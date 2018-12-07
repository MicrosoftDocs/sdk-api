---
UID: NL:gdipluspath.GraphicsPath
title: GraphicsPath
author: windows-sdk-content
description: A GraphicsPath object stores a sequence of lines, curves, and shapes.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspath.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GraphicsPath, GraphicsPath class [GDI+], GraphicsPath class [GDI+],described, _gdiplus_CLASS_GraphicsPath_Class, gdiplus._gdiplus_CLASS_GraphicsPath_Class, gdipluspath/GraphicsPath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: class
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GraphicsPath class


## -description


A <a href="https://msdn.microsoft.com/en-us/library/ms535523(v=VS.85).aspx">GraphicsPath</a> object stores a sequence of lines, curves, and shapes. You can draw the entire sequence by calling the 
			<b>DrawPath</b> method of a 
			<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object. You can partition the sequence of lines, curves, and shapes into figures, and with the help of a 
			<a href="https://msdn.microsoft.com/en-us/library/ms534458(v=VS.85).aspx">GraphicsPathIterator</a> object, you can draw selected figures. You can also place markers in the sequence, so that you can draw selected portions of the path.


## -remarks



A path consists of one or more figures. As you add lines and curves to a path, those lines and curves become part of a figure. You can start a new figure by calling the <a href="https://msdn.microsoft.com/en-us/library/ms535569(v=VS.85).aspx">GraphicsPath::StartFigure</a> method. When you draw a path, the lines and curves within an individual figure are connected by straight lines; the ending point of one line or curve is connected to the starting point of the next line or curve. No connecting line is drawn between the end of one figure and the start of the next figure.

A figure can be open or closed. You can close a figure by calling the <a href="https://msdn.microsoft.com/en-us/library/ms535529(v=VS.85).aspx">GraphicsPath::CloseFigure</a> method. After you call <b>GraphicsPath::CloseFigure</b>, the next line, curve, or shape that you add to the path is part of the next figure. When you draw a path, the ending point of each closed figure is automatically connected to the starting point of that figure.

Some shapes (for example, rectangles and ellipses) are intrinsically closed. When you add an intrinsically closed shape to a path, that shape is in a figure by itself, and that figure is considered closed even if you don't call <a href="https://msdn.microsoft.com/en-us/library/ms535529(v=VS.85).aspx">GraphicsPath::CloseFigure</a>. The following methods add intrinsically closed figures to a path: 

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms535540(v=VS.85).aspx">AddClosedCurve Methods</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms535542(v=VS.85).aspx">AddEllipse Methods</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms535545(v=VS.85).aspx">AddPie Methods</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms535546(v=VS.85).aspx">AddPolygon Methods</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms535547(v=VS.85).aspx">AddRectangle Methods</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms535548(v=VS.85).aspx">AddRectangles Methods</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms535549(v=VS.85).aspx">AddString Methods</a>
</li>
</ul>


