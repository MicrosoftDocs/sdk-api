---
UID: NF:gdipluspath.GraphicsPath.GetLastStatus
title: GraphicsPath::GetLastStatus
author: windows-sdk-content
description: The GraphicsPath::GetLastStatus method returns a value that indicates the nature of this GraphicsPath object's most recent method failure.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GetLastStatus_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\getlaststatus_91.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],GetLastStatus method, GraphicsPath.GetLastStatus, GraphicsPath::GetLastStatus, _gdiplus_CLASS_GraphicsPath_GetLastStatus_, gdiplus._gdiplus_CLASS_GraphicsPath_GetLastStatus_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdipluspath.h
req.include-header: Gdiplus.h
req.redist: 
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
 - GraphicsPath.GetLastStatus
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# GraphicsPath::GetLastStatus


## -description


The <b>GraphicsPath::GetLastStatus</b> method returns a value that indicates the nature of this <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object's most recent method failure.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

The <b>GraphicsPath::GetLastStatus</b> method returns an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If no methods invoked on this <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object have failed since the previous call to <b>GraphicsPath::GetLastStatus</b>, then <b>GraphicsPath::GetLastStatus</b> returns Ok.

If at least one method invoked on this <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object has failed since the previous call to <b>GraphicsPath::GetLastStatus</b>, then <b>GraphicsPath::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.




## -remarks



You can call <b>GraphicsPath::GetLastStatus</b> immediately after constructing a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object to determine whether the constructor succeeded.

The first time you call the <b>GraphicsPath::GetLastStatus</b> method of a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object, it returns Ok if the constructor succeeded and all methods invoked so far on the <b>GraphicsPath</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.




## -see-also




<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>



<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a>
 

 

