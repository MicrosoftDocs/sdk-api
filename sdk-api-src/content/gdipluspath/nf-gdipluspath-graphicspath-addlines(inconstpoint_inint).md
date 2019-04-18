---
UID: NF:gdipluspath.GraphicsPath.AddLines(IN const Point,IN INT)
title: GraphicsPath::AddLines(IN const Point,IN INT) (gdipluspath.h)
author: windows-sdk-content
description: The GraphicsPath::AddLines method adds a sequence of connected lines to the current figure of this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddLines_Point_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddlinesmethods\addlines.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddLines, AddLines method [GDI+], AddLines method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddLines method, GraphicsPath.AddLines, GraphicsPath.AddLines(IN const Point,IN INT), GraphicsPath.AddLines(const Point*,INT), GraphicsPath::AddLines, GraphicsPath::AddLines(IN const Point,IN INT), _gdiplus_CLASS_GraphicsPath_AddLines_Point_points_INT_count_, gdiplus._gdiplus_CLASS_GraphicsPath_AddLines_Point_points_INT_count_
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
ms.custom: 19H1
---

# GraphicsPath::AddLines(IN const Point,IN INT)


## -description


The <b>GraphicsPath::AddLines</b> method adds a sequence of connected lines to the current figure of this path.


## -parameters




### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>*</b>

Pointer to an array of points that specify the starting and ending points of the lines. The first point in the array is the starting point of the first line, and the last point in the array is the ending point of the last line. Each of the other points serves as ending point for one line and starting point for the next line. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>points</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms535543(v=VS.85).aspx">AddLine Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535544(v=VS.85).aspx">AddLines Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533855(v=VS.85).aspx">Using a Pen to Draw Lines and Rectangles</a>
 

 

