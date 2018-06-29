---
UID: NF:gdipluspath.GraphicsPath.SetMarker
title: GraphicsPath::SetMarker
author: windows-sdk-content
description: The GraphicsPath::SetMarker method designates the last point in this path as a marker point.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_SetMarker_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\setmarker.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GraphicsPath class [GDI+],SetMarker method, GraphicsPath.SetMarker, GraphicsPath::SetMarker, SetMarker, SetMarker method [GDI+], SetMarker method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_SetMarker_, gdiplus._gdiplus_CLASS_GraphicsPath_SetMarker_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdipluspath.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
tech.root: 
req.typenames: WmfPlaceableFileHeader
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - GraphicsPath.SetMarker
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# GraphicsPath::SetMarker


## -description


The <b>GraphicsPath::SetMarker</b> method designates the last point in this path as a marker point.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



A <a href="https://msdn.microsoft.com/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="https://msdn.microsoft.com/library/ms534162(v=VS.85).aspx">PathPointType</a> enumeration.

Each time you add a line, curve, or shape to a path, the point array and the type array are expanded. When you call <b>GraphicsPath::SetMarker</b>, a marker flag is placed in the last byte of the type array. That flag designates the last point of the point array as a marker point.

Markers divide a path into sections. You can use a <a href="https://msdn.microsoft.com/library/ms534458(v=VS.85).aspx">GraphicsPathIterator</a> object to draw selected sections of a path.




## -see-also




<a href="https://msdn.microsoft.com/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/library/ms535529(v=VS.85).aspx">GraphicsPath::CloseFigure</a>



<a href="https://msdn.microsoft.com/library/ms535535(v=VS.85).aspx">GraphicsPath::GetPathTypes</a>



<a href="https://msdn.microsoft.com/library/ms535569(v=VS.85).aspx">GraphicsPath::StartFigure</a>



<a href="https://msdn.microsoft.com/library/ms534458(v=VS.85).aspx">GraphicsPathIterator</a>



<a href="https://msdn.microsoft.com/library/ms535457(v=VS.85).aspx">GraphicsPathIterator::NextMarker Methods</a>



<a href="https://msdn.microsoft.com/library/ms535458(v=VS.85).aspx">GraphicsPathIterator::NextSubpath Methods</a>



<a href="https://msdn.microsoft.com/library/ms536370(v=VS.85).aspx">Paths</a>
 

 

