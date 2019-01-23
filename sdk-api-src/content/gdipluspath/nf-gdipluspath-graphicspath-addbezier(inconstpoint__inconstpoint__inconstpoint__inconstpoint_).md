---
UID: NF:gdipluspath.GraphicsPath.AddBezier(IN const Point &,IN const Point &,IN const Point &,IN const Point &)
title: GraphicsPath::AddBezier(IN const Point &,IN const Point &,IN const Point &,IN const Point &)
author: windows-sdk-content
description: The GraphicsPath::AddBezier method adds a B&#233;zier spline to the current figure of this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddBezier_Point_pt1_Point_pt2_Point_pt3_Point_pt4_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddbeziermethods\addbezier.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddBezier, AddBezier method [GDI+], AddBezier method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddBezier method, GraphicsPath.AddBezier, GraphicsPath.AddBezier(IN const Point &,IN const Point &,IN const Point &,IN const Point &), GraphicsPath.AddBezier(const Point&,const Point&,const Point&,const Point&), GraphicsPath::AddBezier, GraphicsPath::AddBezier(IN const Point &,IN const Point &,IN const Point &,IN const Point &), _gdiplus_CLASS_GraphicsPath_AddBezier_Point_pt1_Point_pt2_Point_pt3_Point_pt4_, gdiplus._gdiplus_CLASS_GraphicsPath_AddBezier_Point_pt1_Point_pt2_Point_pt3_Point_pt4_
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
 - GraphicsPath.AddBezier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::AddBezier(IN const Point &,IN const Point &,IN const Point &,IN const Point &)


## -description


The <b>GraphicsPath::AddBezier</b> method adds a Bézier spline to the current figure of this path.


## -parameters




### -param pt1 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a></b>

Reference to a point at which to start the Bézier spline. 


### -param pt2 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a></b>

Reference to a point that is the first control point of the Bézier spline. 


### -param pt3 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a></b>

Reference to a point that is the second control point of the Bézier spline. 


### -param pt4 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a></b>

Reference to a point at which to end the Bézier spline. 


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



<a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>
 

 

