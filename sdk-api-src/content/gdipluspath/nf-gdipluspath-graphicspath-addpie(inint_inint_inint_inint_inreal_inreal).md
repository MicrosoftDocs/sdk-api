---
UID: NF:gdipluspath.GraphicsPath.AddPie(IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL)
title: GraphicsPath::AddPie(IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL) (gdipluspath.h)
author: windows-sdk-content
description: The GraphicsPath::AddPie method adds a pie to this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddPie_INT_x_INT_y_INT_width_INT_height_REAL_startAngle_REAL_sweepAngle_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddpiemethods\addpie_5intx_inty_intwidth_intheight_realstarta.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddPie, AddPie method [GDI+], AddPie method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddPie method, GraphicsPath.AddPie, GraphicsPath.AddPie(IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL), GraphicsPath.AddPie(INT,INT,INT,INT,REAL,REAL), GraphicsPath::AddPie, GraphicsPath::AddPie(IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL), _gdiplus_CLASS_GraphicsPath_AddPie_INT_x_INT_y_INT_width_INT_height_REAL_startAngle_REAL_sweepAngle_, gdiplus._gdiplus_CLASS_GraphicsPath_AddPie_INT_x_INT_y_INT_width_INT_height_REAL_startAngle_REAL_sweepAngle_
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
 - GraphicsPath.AddPie
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::AddPie(IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL)


## -description


The <b>GraphicsPath::AddPie</b> method adds a pie to this path. An arc is a portion of an ellipse, and a pie is a portion of the area enclosed by an ellipse. A pie is bounded by an arc and two lines (edges) that go from the center of the ellipse to the endpoints of the arc.


## -parameters




### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the upper-left corner of the rectangle that bounds the ellipse that bounds the pie. 


### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the upper-left corner of the rectangle that bounds the ellipse that bounds the pie. 


### -param width [in]

Type: <b>INT</b>

Integer that specifies the width of the rectangle that bounds the ellipse that bounds the pie. 


### -param height [in]

Type: <b>INT</b>

Integer that specifies the height of the rectangle that bounds the ellipse that bounds the pie. 


### -param startAngle [in]

Type: <b>REAL</b>

Real number that specifies the clockwise angle, in degrees, between the horizontal axis of the ellipse and the starting point of the arc that defines the pie. 


### -param sweepAngle [in]

Type: <b>REAL</b>

Real number that specifies the clockwise angle, in degrees, between the starting and ending points of the arc that defines the pie. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms535537(v=VS.85).aspx">AddArc Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535545(v=VS.85).aspx">AddPie Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535733(v=VS.85).aspx">DrawArc Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535751(v=VS.85).aspx">DrawPie Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536362(v=VS.85).aspx">Ellipses and Arcs</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536366(v=VS.85).aspx">Open and Closed Curves</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>
 

 

