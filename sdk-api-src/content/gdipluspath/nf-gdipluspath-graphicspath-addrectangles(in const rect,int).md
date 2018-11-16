---
UID: NF:gdipluspath.GraphicsPath.AddRectangles(IN const Rect,INT)
title: GraphicsPath::AddRectangles(IN const Rect,INT)
author: windows-sdk-content
description: The GraphicsPath::AddRectangles method adds a sequence of rectangles to this path
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddRectangles_Rect_rects_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddrectanglesmethods\addrectangles.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AddRectangles, AddRectangles method [GDI+], AddRectangles method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddRectangles method, GraphicsPath.AddRectangles, GraphicsPath.AddRectangles(IN const Rect,INT), GraphicsPath.AddRectangles(const Rect*,INT), GraphicsPath::AddRectangles, GraphicsPath::AddRectangles(IN const Rect,INT), _gdiplus_CLASS_GraphicsPath_AddRectangles_Rect_rects_INT_count_, gdiplus._gdiplus_CLASS_GraphicsPath_AddRectangles_Rect_rects_INT_count_
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - GraphicsPath.AddRectangles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdipluspath.h
: 
- GraphicsPath.AddRectangles
: 
req.product: GDI+ 1.0
---

# GraphicsPath::AddRectangles(IN const Rect,INT)


## -description


The <b>GraphicsPath::AddRectangles</b> method adds a sequence of rectangles to this path


## -parameters




### -param rects [in]

Type: <b>const <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>*</b>

Pointer to an array of rectangles that will be added to the path. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>rects</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/b86c87c0-7d6b-4e9d-b276-a98ac9a33772">AddRectangle Methods</a>



<a href="https://msdn.microsoft.com/467d4a61-8430-403c-90ed-f8c224ce3b61">AddRectangles Methods</a>



<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/f2e4144f-f2f1-49db-bfdf-ffce3023b4cb">Using a Pen to Draw Lines and Rectangles</a>
 

 

