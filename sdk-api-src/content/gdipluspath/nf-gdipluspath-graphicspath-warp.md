---
UID: NF:gdipluspath.GraphicsPath.Warp
title: GraphicsPath::Warp (gdipluspath.h)
description: The GraphicsPath::Warp method applies a warp transformation to this path. The GraphicsPath::Warp method also flattens (converts to a sequence of straight lines) the path.
helpviewer_keywords: ["GraphicsPath class [GDI+]","Warp method","GraphicsPath.Warp","GraphicsPath::Warp","Warp","Warp method [GDI+]","Warp method [GDI+]","GraphicsPath class","_gdiplus_CLASS_GraphicsPath_Warp_destPoints_count_srcRect_matrix_warpMode_flatness_","gdiplus._gdiplus_CLASS_GraphicsPath_Warp_destPoints_count_srcRect_matrix_warpMode_flatness_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_Warp_destPoints_count_srcRect_matrix_warpMode_flatness_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\warp.htm
ms.date: 12/05/2018
ms.keywords: GraphicsPath class [GDI+],Warp method, GraphicsPath.Warp, GraphicsPath::Warp, Warp, Warp method [GDI+], Warp method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_Warp_destPoints_count_srcRect_matrix_warpMode_flatness_, gdiplus._gdiplus_CLASS_GraphicsPath_Warp_destPoints_count_srcRect_matrix_warpMode_flatness_
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
 - GraphicsPath::Warp
 - gdipluspath/GraphicsPath::Warp
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
 - GraphicsPath.Warp
---

# GraphicsPath::Warp


## -description

The <b>GraphicsPath::Warp</b> method applies a warp transformation to this path. The <b>GraphicsPath::Warp</b> method also flattens (converts to a sequence of straight lines) the path.

## -parameters

### -param destPoints [in]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>*</b>

Pointer to an array of points that, along with the <i>srcRect</i> parameter, defines the warp transformation.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of points in the 
					<i>destPoints</i> array. The value of this parameter must be 3 or 4.

### -param srcRect [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a></b>

Reference to a rectangle that, along with the <i>destPoints</i> parameter, defines the warp transformation.

### -param matrix [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Optional. Pointer to a <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that represents a transformation to be applied along with the warp. If this parameter is <b>NULL</b>, no transformation is applied. The default value is <b>NULL</b>.

### -param warpMode [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-warpmode">WarpMode</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-warpmode">WarpMode</a> enumeration that specifies the kind of warp to be applied. The default value is WarpModePerspective.

### -param flatness [in]

Type: <b>REAL</b>

Optional. Real number that influences the number of line segments that are used to approximate the original path. Small values specify that many line segments are used, and large values specify that few line segments are used. The default value is FlatnessDefault, which is a constant defined in Gdiplusenums.h.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object stores a collection of data points that represent lines and curves. The <b>GraphicsPath::Warp</b> method converts those data points so that they represent only lines. The <i>flatness</i> parameter influences the number of lines that are stored. The original data points that represented curves are lost.

If the 
				<i>count</i> parameter has a value of 4, the warp transformation is defined as shown in the following table.

<table>
<tr>
<th>Source point</th>
<th>Destination point</th>
</tr>
<tr>
<td>Upper-left corner of <i>srcRect</i></td>
<td><i>destPoints</i>[0]</td>
</tr>
<tr>
<td>Upper-right corner of <i>srcRect</i></td>
<td><i>destPoints</i>[1]</td>
</tr>
<tr>
<td>Lower-left corner of <i>srcRect</i></td>
<td><i>destPoints</i>[2]</td>
</tr>
<tr>
<td>Lower-right corner of <i>srcRect</i></td>
<td><i>destPoints</i>[3]</td>
</tr>
</table>
 

A transformation specified by a source rectangle and four destination points is capable of mapping a rectangle to an arbitrary quadrilateral that is not necessarily a parallelogram.

If the count parameter has a value of 3, the warp transformation is defined as shown in the following table.

<table>
<tr>
<th>Source point</th>
<th>Destination point</th>
</tr>
<tr>
<td>Upper-left corner of 
							<i>srcRect</i></td>
<td><i>destPoints</i>[0]</td>
</tr>
<tr>
<td>Upper-right corner of 
							<i>srcRect</i></td>
<td><i>destPoints</i>[1]</td>
</tr>
<tr>
<td>Lower-left corner of 
							<i>srcRect</i></td>
<td><i>destPoints</i>[2]</td>
</tr>
</table>
 

A transformation specified by a source rectangle and three destination points maps rectangles to parallelograms.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object and adds a closed figure to the path. The code defines a warp transformation by specifying a source rectangle and an array of four destination points. The source rectangle and destination points are passed to the <b>Warp</b> method. The code draws the path twice: once before it has been warped and once after it has been warped.


```cpp

VOID WarpExample(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path.
   PointF points[] ={
      PointF(20.0f, 60.0f),
      PointF(30.0f, 90.0f),
      PointF(15.0f, 110.0f),
      PointF(15.0f, 145.0f),
      PointF(55.0f, 145.0f),
      PointF(55.0f, 110.0f),
      PointF(40.0f, 90.0f),
      PointF(50.0f, 60.0f)};

   GraphicsPath path;
   path.AddLines(points, 8);
   path.CloseFigure();

   // Draw the path before applying a warp transformation.
   Pen bluePen(Color(255, 0, 0, 255));
   graphics.DrawPath(&bluePen, &path);

   // Define a warp transformation, and warp the path.
   RectF srcRect(10.0f, 50.0f, 50.0f, 100.0f);

   PointF destPts[] = {
      PointF(220.0f, 10.0f),
      PointF(280.0f, 10.0f),
      PointF(100.0f, 150.0f),
      PointF(400.0f, 150.0f)};

   path.Warp(destPts, 4, srcRect);

   // Draw the warped path.
   graphics.DrawPath(&bluePen, &path);

   // Draw the source rectangle and the destination polygon.
   Pen blackPen(Color(255, 0, 0, 0));
   graphics.DrawRectangle(&blackPen, srcRect);
   graphics.DrawLine(&blackPen, destPts[0], destPts[1]);
   graphics.DrawLine(&blackPen, destPts[0], destPts[2]);
   graphics.DrawLine(&blackPen, destPts[1], destPts[3]);
   graphics.DrawLine(&blackPen, destPts[2], destPts[3]);
}

```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-flattening-paths-about">Flattening Paths</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-flatten">GraphicsPath::Flatten</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-outline">GraphicsPath::Outline</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-widen">GraphicsPath::Widen</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-warpmode">WarpMode</a>