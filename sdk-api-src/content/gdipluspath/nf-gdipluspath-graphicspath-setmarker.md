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
req.typenames: WmfPlaceableFileHeader
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	GraphicsPath.SetMarker
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



A <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="https://msdn.microsoft.com/daad4301-f338-4cce-bb31-ddcf09c0c59c">PathPointType</a> enumeration.

Each time you add a line, curve, or shape to a path, the point array and the type array are expanded. When you call <b>GraphicsPath::SetMarker</b>, a marker flag is placed in the last byte of the type array. That flag designates the last point of the point array as a marker point.

Markers divide a path into sections. You can use a <a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a> object to draw selected sections of a path.




## -see-also




<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/8f828820-7dd6-4dd0-959c-4dcfb1ca6ac7">GraphicsPath::CloseFigure</a>



<a href="https://msdn.microsoft.com/fded6e62-0134-4e2c-aa40-cf0a32a5b2f2">GraphicsPath::GetPathTypes</a>



<a href="https://msdn.microsoft.com/3c503ff5-6f20-45bd-b61e-13dd0f3efca5">GraphicsPath::StartFigure</a>



<a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a>



<a href="https://msdn.microsoft.com/6eb9e19c-df28-4cf9-a434-c27478ba1fa5">GraphicsPathIterator::NextMarker Methods</a>



<a href="https://msdn.microsoft.com/91137029-182d-4dc5-89a3-f3835f55d327">GraphicsPathIterator::NextSubpath Methods</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>
 

 

