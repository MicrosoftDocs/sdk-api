---
UID: NF:gdipluspath.GraphicsPath.AddArc(IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL)
title: GraphicsPath::AddArc(IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL)
author: windows-sdk-content
description: The GraphicsPath::AddArc method adds an elliptical arc to the current figure of this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddArc_INT_x_INT_y_INT_width_INT_height_REAL_startAngle_REAL_sweepAngle_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddarcmethods\addarc_35intx_inty_intwidth_intheight_realstart.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AddArc, AddArc method [GDI+], AddArc method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddArc method, GraphicsPath.AddArc, GraphicsPath.AddArc(IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL), GraphicsPath.AddArc(INT,INT,INT,INT,REAL,REAL), GraphicsPath::AddArc, GraphicsPath::AddArc(IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL), _gdiplus_CLASS_GraphicsPath_AddArc_INT_x_INT_y_INT_width_INT_height_REAL_startAngle_REAL_sweepAngle_, gdiplus._gdiplus_CLASS_GraphicsPath_AddArc_INT_x_INT_y_INT_width_INT_height_REAL_startAngle_REAL_sweepAngle_
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
 - GraphicsPath.AddArc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::AddArc(IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL)


## -description


The <b>GraphicsPath::AddArc</b> method adds an elliptical arc to the current figure of this path.


## -parameters




### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the upper-left corner of the bounding rectangle for the ellipse that contains the arc. 


### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the upper-left corner of the bounding rectangle for the ellipse that contains the arc. 


### -param width [in]

Type: <b>INT</b>

Integer that specifies the width of the bounding rectangle for the ellipse that contains the arc. 


### -param height [in]

Type: <b>INT</b>

Integer that specifies the height of the bounding rectangle for the ellipse that contains the arc. 


### -param startAngle [in]

Type: <b>REAL</b>

Real number that specifies the clockwise angle, in degrees, between the horizontal axis of the ellipse and the starting point of the arc. 


### -param sweepAngle [in]

Type: <b>REAL</b>

Real number that specifies the clockwise angle, in degrees, between the starting point (<i>startAngle</i>) and ending point of the arc. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/54171039-4cb9-4898-a656-b7a9df4b18f6">AddArc Methods</a>



<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/b30757ea-b8b8-45bd-a716-a4c8c9c5f1ec">DrawArc Methods</a>



<a href="https://msdn.microsoft.com/45e80501-4d64-480b-a7c7-3af52c00a0aa">Ellipses and Arcs</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>
 

 

