---
UID: NF:gdipluspath.GraphicsPath.AddBeziers(IN const Point,IN INT)
title: GraphicsPath::AddBeziers(IN const Point,IN INT)
author: windows-sdk-content
description: The GraphicsPath::AddBeziers method adds a sequence of connected B&#233;zier splines to the current figure of this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddBeziers_PointF_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddbeziersmethods\addbeziers_6pointfpoints_intcount.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddBeziers, AddBeziers method [GDI+], AddBeziers method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddBeziers method, GraphicsPath.AddBeziers, GraphicsPath.AddBeziers(IN const Point,IN INT), GraphicsPath.AddBeziers(const PointF*,INT), GraphicsPath::AddBeziers, GraphicsPath::AddBeziers(IN const Point,IN INT), _gdiplus_CLASS_GraphicsPath_AddBeziers_PointF_points_INT_count_, gdiplus._gdiplus_CLASS_GraphicsPath_AddBeziers_PointF_points_INT_count_
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
 - GraphicsPath.AddBeziers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::AddBeziers(IN const Point,IN INT)


## -description


The <b>GraphicsPath::AddBeziers</b> method adds a sequence of connected Bézier splines to the current figure of this path.


## -parameters




### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>*</b>

Pointer to an array of starting points, ending points, and control points for the connected splines. The first spline is constructed from the first point through the fourth point in the array and uses the second and third points as control points. Each subsequent spline in the sequence needs exactly three more points: the ending point of the previous spline is used as the starting point, the next two points in the sequence are control points, and the third point is the ending point. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>points</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms535538(v=VS.85).aspx">AddBezier Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535539(v=VS.85).aspx">AddBeziers Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535541(v=VS.85).aspx">AddCurve Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536354(v=VS.85).aspx">Bézier Splines</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533926(v=VS.85).aspx">Drawing Bézier Splines</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>
 

 

