---
UID: NF:gdipluspath.GraphicsPath.AddBezier(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)
title: GraphicsPath::AddBezier(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL) (gdipluspath.h)
author: windows-sdk-content
description: The GraphicsPath::AddBezier method adds a B&#233;zier spline to the current figure of this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddBezier_REAL_x1_REAL_y1_REAL_x2_REAL_y2_REAL_x3_REAL_y3_REAL_x4_REAL_y.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddbeziermethods\addbezier_43realx1_realy1_realx2_realy2_realx3_rea.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddBezier, AddBezier method [GDI+], AddBezier method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddBezier method, GraphicsPath.AddBezier, GraphicsPath.AddBezier(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), GraphicsPath.AddBezier(REAL,REAL,REAL,REAL,REAL,REAL,REAL,REAL), GraphicsPath::AddBezier, GraphicsPath::AddBezier(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), _gdiplus_CLASS_GraphicsPath_AddBezier_REAL_x1_REAL_y1_REAL_x2_REAL_y2_REAL_x3_REAL_y3_REAL_x4_REAL_y, gdiplus._gdiplus_CLASS_GraphicsPath_AddBezier_REAL_x1_REAL_y1_REAL_x2_REAL_y2_REAL_x3_REAL_y3_REAL_x4_REAL_y
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
ms.custom: 19H1
---

# GraphicsPath::AddBezier(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)


## -description


The <b>GraphicsPath::AddBezier</b> method adds a Bézier spline to the current figure of this path.


## -parameters




### -param x1 [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the starting point of the Bézier spline. 


### -param y1 [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the starting point of the Bézier spline. 


### -param x2 [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the first control point of the Bézier spline. 


### -param y2 [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the first control point of the Bézier spline. 


### -param x3 [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the second control point of the Bézier spline. 


### -param y3 [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the second control point of the Bézier spline. 


### -param x4 [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the ending point of the Bézier spline. 


### -param y4 [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the ending point of the Bézier spline. 


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
 

 

