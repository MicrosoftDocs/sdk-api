---
UID: NF:gdipluspath.GraphicsPath.AddPie(INREAL,INREAL,INREAL,INREAL,INREAL,INREAL)
title: GraphicsPath::AddPie(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL) (gdipluspath.h)
description: The GraphicsPath::AddPie method adds a pie to this path.
helpviewer_keywords: ["AddPie","AddPie method [GDI+]","AddPie method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","AddPie method","GraphicsPath.AddPie","GraphicsPath.AddPie(IN REAL","IN REAL","IN REAL","IN REAL","IN REAL","IN REAL)","GraphicsPath.AddPie(REAL","REAL","REAL","REAL","REAL","REAL)","GraphicsPath::AddPie","GraphicsPath::AddPie(IN REAL","IN REAL","IN REAL","IN REAL","IN REAL","IN REAL)","_gdiplus_CLASS_GraphicsPath_AddPie_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sweepAn","gdiplus._gdiplus_CLASS_GraphicsPath_AddPie_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sweepAn"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddPie_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sweepAn.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddpiemethods\addpie_62realx_realy_realwidth_realheight_reals.htm
ms.date: 12/05/2018
ms.keywords: AddPie, AddPie method [GDI+], AddPie method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddPie method, GraphicsPath.AddPie, GraphicsPath.AddPie(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), GraphicsPath.AddPie(REAL,REAL,REAL,REAL,REAL,REAL), GraphicsPath::AddPie, GraphicsPath::AddPie(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), _gdiplus_CLASS_GraphicsPath_AddPie_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sweepAn, gdiplus._gdiplus_CLASS_GraphicsPath_AddPie_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sweepAn
f1_keywords:
- gdipluspath/GraphicsPath.AddPie
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# GraphicsPath::AddPie(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)


## -description


The <b>GraphicsPath::AddPie</b> method adds a pie to this path. An arc is a portion of an ellipse, and a pie is a portion of the area enclosed by an ellipse. A pie is bounded by an arc and two lines (edges) that go from the center of the ellipse to the endpoints of the arc.


## -parameters




### -param x [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the upper-left corner of the rectangle that bounds the ellipse that bounds the pie. 


### -param y [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the upper-left corner of the rectangle that bounds the ellipse that bounds the pie. 


### -param width [in]

Type: <b>REAL</b>

Real number that specifies the width of the rectangle that bounds the ellipse that bounds the pie. 


### -param height [in]

Type: <b>REAL</b>

Real number that specifies the height of the rectangle that bounds the ellipse that bounds the pie. 


### -param startAngle [in]

Type: <b>REAL</b>

Real number that specifies the clockwise angle, in degrees, between the horizontal axis of the ellipse and the starting point of the arc that defines the pie. 


### -param sweepAngle [in]

Type: <b>REAL</b>

Real number that specifies the clockwise angle, in degrees, between the starting and ending points of the arc that defines the pie. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inconstrect__inreal_inreal)">AddArc Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addpie(inconstrect__inreal_inreal)">AddPie Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal)">DrawArc Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpie(inconstpen_inconstrect__inreal_inreal)">DrawPie Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-ellipses-and-arcs-about">Ellipses and Arcs</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-open-and-closed-curves-about">Open and Closed Curves</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>
 

 

