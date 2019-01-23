---
UID: NF:gdipluspath.GraphicsPath.IsOutlineVisible(IN const Point &,IN const Pen,IN const Graphics)
title: GraphicsPath::IsOutlineVisible(IN const Point &,IN const Pen,IN const Graphics)
author: windows-sdk-content
description: The GraphicsPath::IsOutlineVisible method determines whether a specified point touches the outline of this path when the path is drawn by a specified Graphicsobject and a specified pen.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_IsOutlineVisible_Point_point_Pen_pen_Graphics_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathisoutlinevisiblemethods\isoutlinevisible.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GraphicsPath class [GDI+],IsOutlineVisible method, GraphicsPath.IsOutlineVisible, GraphicsPath.IsOutlineVisible(IN const Point &,IN const Pen,IN const Graphics), GraphicsPath.IsOutlineVisible(const Point&,const Pen*,const Graphics*), GraphicsPath::IsOutlineVisible, GraphicsPath::IsOutlineVisible(IN const Point &,IN const Pen,IN const Graphics), IsOutlineVisible, IsOutlineVisible method [GDI+], IsOutlineVisible method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_IsOutlineVisible_Point_point_Pen_pen_Graphics_g_, gdiplus._gdiplus_CLASS_GraphicsPath_IsOutlineVisible_Point_point_Pen_pen_Graphics_g_
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
 - GraphicsPath.IsOutlineVisible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::IsOutlineVisible(IN const Point &,IN const Pen,IN const Graphics)


## -description


The <b>GraphicsPath::IsOutlineVisible</b> method determines whether a specified point touches the outline of this path when the path is drawn by a specified <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>object and a specified pen.


## -parameters




### -param point [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a></b>

Reference to the point to be tested. 


### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object. This method determines whether the test point touches the path outline that would be drawn by this pen. More points will touch an outline drawn by a wide pen than will touch an outline drawn by a narrow pen. 


### -param g [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>*</b>

Optional. Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object that specifies a world-to-device transformation. If the value of this parameter is <b>NULL</b>, the test is done in world coordinates; otherwise, the test is done in device coordinates. The default value is <b>NULL</b>. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the test point touches the outline of this path, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535562(v=VS.85).aspx">IsOutlineVisible Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535563(v=VS.85).aspx">IsVisible Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533854(v=VS.85).aspx">Setting Pen Width and Alignment</a>
 

 

