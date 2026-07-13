---
UID: NF:gdipluspath.GraphicsPath.AddEllipse(REAL,REAL,REAL,REAL)
title: GraphicsPath::AddEllipse(IN REAL,IN REAL,IN REAL,IN REAL) (gdipluspath.h)
description: The GraphicsPath::AddEllipse method adds an ellipse to this path. (overload 1/4)
helpviewer_keywords: ["AddEllipse","AddEllipse method [GDI+]","AddEllipse method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","AddEllipse method","GraphicsPath.AddEllipse","GraphicsPath.AddEllipse(IN REAL","IN REAL","IN REAL","IN REAL)","GraphicsPath.AddEllipse(REAL","REAL","REAL","REAL)","GraphicsPath::AddEllipse","GraphicsPath::AddEllipse(IN REAL","IN REAL","IN REAL","IN REAL)","_gdiplus_CLASS_GraphicsPath_AddEllipse_REAL_x_REAL_y_REAL_width_REAL_height_","gdiplus._gdiplus_CLASS_GraphicsPath_AddEllipse_REAL_x_REAL_y_REAL_width_REAL_height_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddEllipse_REAL_x_REAL_y_REAL_width_REAL_height_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddellipsemethods\addellipse_69realx_realy_realwidth_realheight.htm
ms.date: 12/05/2018
ms.keywords: AddEllipse, AddEllipse method [GDI+], AddEllipse method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddEllipse method, GraphicsPath.AddEllipse, GraphicsPath.AddEllipse(IN REAL,IN REAL,IN REAL,IN REAL), GraphicsPath.AddEllipse(REAL,REAL,REAL,REAL), GraphicsPath::AddEllipse, GraphicsPath::AddEllipse(IN REAL,IN REAL,IN REAL,IN REAL), _gdiplus_CLASS_GraphicsPath_AddEllipse_REAL_x_REAL_y_REAL_width_REAL_height_, gdiplus._gdiplus_CLASS_GraphicsPath_AddEllipse_REAL_x_REAL_y_REAL_width_REAL_height_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - GraphicsPath::AddEllipse
 - gdipluspath/GraphicsPath::AddEllipse
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - GraphicsPath.AddEllipse
---

# GraphicsPath::AddEllipse(IN REAL,IN REAL,IN REAL,IN REAL)


## -description

The <b>GraphicsPath::AddEllipse</b> method adds an ellipse to this path.

## -parameters

### -param x [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the upper-left corner of the bounding rectangle for the ellipse.

### -param y [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the upper-left corner of the bounding rectangle for the ellipse.

### -param width [in]

Type: <b>REAL</b>

Real number that specifies the width of the bounding rectangle for the ellipse.

### -param height [in]

Type: <b>REAL</b>

Real number that specifies the height of the bounding rectangle for the ellipse.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object stores an ellipse as a sequence of four connected Bézier splines. The <b>GraphicsPath</b> object does not store the upper-left corner, width, and height of the ellipse's bounding rectangle.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object <i>path</i>, adds an ellipse to <i>path</i>, and then draws <i>path</i>.


```cpp
VOID Example_AddEllipse(HDC hdc)
{
   Graphics graphics(hdc); 

   GraphicsPath path;
   path.AddEllipse(20.0f, 20.0f, 200.0f, 100.0f);

   // Draw the path.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inconstrect__inreal_inreal)">AddArc Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inconstrect_)">AddEllipse Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-ellipses-and-arcs-about">Ellipses and Arcs</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>
