---
UID: NF:gdipluspath.GraphicsPath.Outline
title: GraphicsPath::Outline (gdipluspath.h)
description: The GraphicsPath::Outline method transforms and flattens this path, and then converts this path's data points so that they represent only the outline of the path.
helpviewer_keywords: ["GraphicsPath class [GDI+]","Outline method","GraphicsPath.Outline","GraphicsPath::Outline","Outline","Outline method [GDI+]","Outline method [GDI+]","GraphicsPath class","_gdiplus_CLASS_GraphicsPath_Outline_matrix_flatness_","gdiplus._gdiplus_CLASS_GraphicsPath_Outline_matrix_flatness_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_Outline_matrix_flatness_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\outline.htm
ms.date: 12/05/2018
ms.keywords: GraphicsPath class [GDI+],Outline method, GraphicsPath.Outline, GraphicsPath::Outline, Outline, Outline method [GDI+], Outline method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_Outline_matrix_flatness_, gdiplus._gdiplus_CLASS_GraphicsPath_Outline_matrix_flatness_
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
 - GraphicsPath::Outline
 - gdipluspath/GraphicsPath::Outline
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
 - GraphicsPath.Outline
---

# GraphicsPath::Outline


## -description

The <b>GraphicsPath::Outline</b> method transforms and flattens this path, and then converts this path's data points so that they represent only the outline of the path.

## -parameters

### -param matrix [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Optional. Pointer to a <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that specifies the transformation. If this parameter is <b>NULL</b>, no transformation is applied. The default value is <b>NULL</b>.

### -param flatness [in]

Type: <b>REAL</b>

Optional. Real number that specifies the maximum error between the path and its flattened approximation. Reducing the flatness increases the number of line segments in the approximation. The default value is FlatnessDefault, which is a constant defined in Gdiplusenums.h.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object stores a collection of data points that represent lines and curves. The <b>GraphicsPath::Outline</b> method changes those data points, and the original data points are lost.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object and calls the <a href="/previous-versions/ms535615(v=vs.85)">GraphicsPath::AddClosedCurve</a> method to add a closed cardinal spline to the path. The code calls the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-widen">GraphicsPath::Widen</a> method to widen the path and then draws the path. Next, the code calls the path's <b>Outline</b> method. The code calls the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform">TranslateTransform</a> method of a Graphics object so that the outlined path drawn by the subsequent call to <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath">DrawPath</a> sits to the right of the first path.


```cpp

VOID OutlineExample(HDC hdc)
{
   Graphics graphics(hdc);

   Pen bluePen(Color(255, 0, 0, 255));
   Pen greenPen(Color(255, 0, 255,  0), 10);

   PointF points[] = {
      PointF(20.0f, 20.0f),
      PointF(160.0f, 100.0f),
      PointF(140.0f, 60.0f),
      PointF(60.0f, 100.0f)};

   GraphicsPath path;
   path.AddClosedCurve(points, 4);

   path.Widen(&greenPen);
   graphics.DrawPath(&bluePen, &path);

   path.Outline();

   graphics.TranslateTransform(180.0f, 0.0f);
   graphics.DrawPath(&bluePen, &path);
}

```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-flatten">GraphicsPath::Flatten</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-warp">GraphicsPath::Warp</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-widen">GraphicsPath::Widen</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>