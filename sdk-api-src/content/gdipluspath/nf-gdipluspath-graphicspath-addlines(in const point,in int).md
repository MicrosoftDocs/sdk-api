---
UID: NF:gdipluspath.GraphicsPath.AddLines(IN const Point,IN INT)
title: GraphicsPath::AddLines(IN const Point,IN INT)
author: windows-sdk-content
description: The GraphicsPath::AddLines method adds a sequence of connected lines to the current figure of this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddLines_Point_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddlinesmethods\addlines.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: AddLines, AddLines method [GDI+], AddLines method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddLines method, GraphicsPath.AddLines, GraphicsPath.AddLines(IN const Point,IN INT), GraphicsPath.AddLines(const Point*,INT), GraphicsPath::AddLines, GraphicsPath::AddLines(IN const Point,IN INT), _gdiplus_CLASS_GraphicsPath_AddLines_Point_points_INT_count_, gdiplus._gdiplus_CLASS_GraphicsPath_AddLines_Point_points_INT_count_
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
 - GraphicsPath.AddLines
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::AddLines(IN const Point,IN INT)


## -description


The <b>GraphicsPath::AddLines</b> method adds a sequence of connected lines to the current figure of this path.


## -parameters




### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>*</b>

Pointer to an array of points that specify the starting and ending points of the lines. The first point in the array is the starting point of the first line, and the last point in the array is the ending point of the last line. Each of the other points serves as ending point for one line and starting point for the next line. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>points</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/ff80b2a7-47a9-49dd-b2ea-9bd0453fac0b">AddLine Methods</a>



<a href="https://msdn.microsoft.com/39055c59-6d88-4b46-bc4c-cf2a4a927d29">AddLines Methods</a>



<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>



<a href="https://msdn.microsoft.com/f2e4144f-f2f1-49db-bfdf-ffce3023b4cb">Using a Pen to Draw Lines and Rectangles</a>
 

 

