---
UID: NF:gdipluspath.GraphicsPath.AddLine(IN const Point &,IN const Point &)
title: GraphicsPath::AddLine(IN const Point &,IN const Point &) (gdipluspath.h)
author: windows-sdk-content
description: The GraphicsPath::AddLine method adds a line to the current figure of this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddLine_Point_pt1_Point_pt2_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddlinemethods\addline.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddLine, AddLine method [GDI+], AddLine method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddLine method, GraphicsPath.AddLine, GraphicsPath.AddLine(IN const Point &,IN const Point &), GraphicsPath.AddLine(const Point&,const Point&), GraphicsPath::AddLine, GraphicsPath::AddLine(IN const Point &,IN const Point &), _gdiplus_CLASS_GraphicsPath_AddLine_Point_pt1_Point_pt2_, gdiplus._gdiplus_CLASS_GraphicsPath_AddLine_Point_pt1_Point_pt2_
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
 - GraphicsPath.AddLine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::AddLine(IN const Point &,IN const Point &)


## -description


The <b>GraphicsPath::AddLine</b> method adds a line to the current figure of this path.


## -parameters




### -param pt1 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a></b>

Reference to a point at which to start the line. 


### -param pt2 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a></b>

Reference to a point at which to end the line. 


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
 

 

