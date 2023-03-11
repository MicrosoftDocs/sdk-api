---
UID: NF:gdipluspath.GraphicsPath.GetBounds(Rect,constMatrix,constPen)
title: GraphicsPath::GetBounds(OUT Rect,IN const Matrix,IN const Pen) (gdipluspath.h)
description: The GraphicsPath::GetBounds method gets a bounding rectangle for this path. (overload 1/2)
helpviewer_keywords: ["GetBounds","GetBounds method [GDI+]","GetBounds method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","GetBounds method","GraphicsPath.GetBounds","GraphicsPath.GetBounds(OUT Rect","IN const Matrix","IN const Pen)","GraphicsPath.GetBounds(Rect*","const Matrix*","const Pen*)","GraphicsPath::GetBounds","GraphicsPath::GetBounds(OUT Rect","IN const Matrix","IN const Pen)","_gdiplus_CLASS_GraphicsPath_GetBounds_Rect_bounds_Matrix_matrix_Pen_pen_","gdiplus._gdiplus_CLASS_GraphicsPath_GetBounds_Rect_bounds_Matrix_matrix_Pen_pen_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GetBounds_Rect_bounds_Matrix_matrix_Pen_pen_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathgetboundsmethods\getbounds.htm
ms.date: 12/05/2018
ms.keywords: GetBounds, GetBounds method [GDI+], GetBounds method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],GetBounds method, GraphicsPath.GetBounds, GraphicsPath.GetBounds(OUT Rect,IN const Matrix,IN const Pen), GraphicsPath.GetBounds(Rect*,const Matrix*,const Pen*), GraphicsPath::GetBounds, GraphicsPath::GetBounds(OUT Rect,IN const Matrix,IN const Pen), _gdiplus_CLASS_GraphicsPath_GetBounds_Rect_bounds_Matrix_matrix_Pen_pen_, gdiplus._gdiplus_CLASS_GraphicsPath_GetBounds_Rect_bounds_Matrix_matrix_Pen_pen_
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
 - GraphicsPath::GetBounds
 - gdipluspath/GraphicsPath::GetBounds
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
 - GraphicsPath.GetBounds
---

# GraphicsPath::GetBounds(OUT Rect,IN const Matrix,IN const Pen)


## -description

The <b>GraphicsPath::GetBounds</b> method gets a bounding rectangle for this path.

## -parameters

### -param bounds [out]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a> object that receives the bounding rectangle.

### -param matrix [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Optional. Pointer to a <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that specifies a transformation to be applied to this path before the bounding rectangle is calculated. This path is not permanently transformed; the transformation is used only during the process of calculating the bounding rectangle. The default value is <b>NULL</b>.

### -param pen [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Optional. Pointer to a <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object that influences the size of the bounding rectangle. The bounding rectangle received in <i>bounds</i> will be large enough to enclose this path when the path is drawn with the pen specified by this parameter. This ensures that the path is enclosed by the bounding rectangle even if the path is drawn with a wide pen. The default value is <b>NULL</b>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The rectangle returned by this method might be larger than necessary to enclose the path as drawn by the specified pen. The rectangle is calculated to allow for the pen's miter limit at sharp corners and to allow for the pen's end caps.


#### Examples



The following example creates a path that has one curve and one ellipse. The code draws the path with a thick yellow pen and a thin black pen. The <b>GraphicsPath::GetBounds</b> method receives the address of the thick yellow pen and calculates a bounding rectangle for the path. Then the code draws the bounding rectangle.


```cpp
VOID GetBoundsExample(HDC hdc)
{
   Graphics graphics(hdc);
   Pen blackPen(Color(255, 0, 0, 0), 1);
   Pen yellowPen(Color(255, 255, 255, 0), 10);
   Pen redPen(Color(255, 255, 0, 0), 1);

   Point pts[] = {Point(120,120), 
                  Point(200,130), 
                  Point(150,200), 
                  Point(130,180)};

   // Create a path that has one curve and one ellipse.
   GraphicsPath path;
   path.AddClosedCurve(pts, 4);
   path.AddEllipse(120, 220, 100, 40);

   // Draw the path with a thick yellow pen and a thin black pen.
   graphics.DrawPath(&yellowPen, &path);
   graphics.DrawPath(&blackPen, &path);
 
   // Get the path's bounding rectangle.
   Rect rect;
   path.GetBounds(&rect, NULL, &yellowPen);
   graphics.DrawRectangle(&redPen, rect);  
}

Color(255, 0, 0, 0)Color(255, 255, 0,  0)
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>
