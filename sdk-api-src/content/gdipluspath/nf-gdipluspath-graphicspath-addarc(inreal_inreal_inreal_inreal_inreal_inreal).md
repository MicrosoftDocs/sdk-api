---
UID: NF:gdipluspath.GraphicsPath.AddArc(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)
title: GraphicsPath::AddArc(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL) (gdipluspath.h)
author: windows-sdk-content
description: The GraphicsPath::AddArc method adds an elliptical arc to the current figure of this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddArc_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sweepAn.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddarcmethods\addarc_3realx_realy_realwidth_realheight_realst.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddArc, AddArc method [GDI+], AddArc method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddArc method, GraphicsPath.AddArc, GraphicsPath.AddArc(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), GraphicsPath.AddArc(REAL,REAL,REAL,REAL,REAL,REAL), GraphicsPath::AddArc, GraphicsPath::AddArc(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), _gdiplus_CLASS_GraphicsPath_AddArc_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sweepAn, gdiplus._gdiplus_CLASS_GraphicsPath_AddArc_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sweepAn
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
 - GraphicsPath.AddArc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# GraphicsPath::AddArc(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)


## -description


The <b>GraphicsPath::AddArc</b> method adds an elliptical arc to the current figure of this path.


## -parameters




### -param x [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the upper-left corner of the bounding rectangle for the ellipse that contains the arc. 


### -param y [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the upper-left corner of the bounding rectangle for the ellipse that contains the arc. 


### -param width [in]

Type: <b>REAL</b>

Real number that specifies the width of the bounding rectangle for the ellipse that contains the arc. 


### -param height [in]

Type: <b>REAL</b>

Real number that specifies the height of the bounding rectangle for the ellipse that contains the arc. 


### -param startAngle [in]

Type: <b>REAL</b>

Real number that specifies the clockwise angle, in degrees, between the horizontal axis of the ellipse and the starting point of the arc. 


### -param sweepAngle [in]

Type: <b>REAL</b>

Real number that specifies the clockwise angle, in degrees, between the starting point (<i>startAngle</i>) and the ending point of the arc. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms535537(v=VS.85).aspx">AddArc Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535733(v=VS.85).aspx">DrawArc Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536362(v=VS.85).aspx">Ellipses and Arcs</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>
 

 

