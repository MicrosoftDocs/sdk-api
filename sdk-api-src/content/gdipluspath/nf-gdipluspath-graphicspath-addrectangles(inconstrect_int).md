---
UID: NF:gdipluspath.GraphicsPath.AddRectangles(IN const Rect,INT)
title: GraphicsPath::AddRectangles(IN const Rect,INT)
author: windows-sdk-content
description: The GraphicsPath::AddRectangles method adds a sequence of rectangles to this path
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddRectangles_Rect_rects_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddrectanglesmethods\addrectangles.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddRectangles, AddRectangles method [GDI+], AddRectangles method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddRectangles method, GraphicsPath.AddRectangles, GraphicsPath.AddRectangles(IN const Rect,INT), GraphicsPath.AddRectangles(const Rect*,INT), GraphicsPath::AddRectangles, GraphicsPath::AddRectangles(IN const Rect,INT), _gdiplus_CLASS_GraphicsPath_AddRectangles_Rect_rects_INT_count_, gdiplus._gdiplus_CLASS_GraphicsPath_AddRectangles_Rect_rects_INT_count_
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
req.product: GDI+ 1.0
---

# GraphicsPath::AddRectangles(IN const Rect,INT)


## -description


The <b>GraphicsPath::AddRectangles</b> method adds a sequence of rectangles to this path


## -parameters




### -param rects [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>*</b>

Pointer to an array of rectangles that will be added to the path. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>rects</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms535547(v=VS.85).aspx">AddRectangle Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535548(v=VS.85).aspx">AddRectangles Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533855(v=VS.85).aspx">Using a Pen to Draw Lines and Rectangles</a>
 

 

