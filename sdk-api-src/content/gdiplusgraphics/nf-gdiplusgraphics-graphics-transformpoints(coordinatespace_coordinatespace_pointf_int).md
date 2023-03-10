---
UID: NF:gdiplusgraphics.Graphics.TransformPoints(CoordinateSpace,CoordinateSpace,PointF,INT)
title: Graphics::TransformPoints (gdiplusgraphics.h)
description: The Graphics::TransformPoints method converts an array of points from one coordinate space to another. The conversion is based on the current world and page transformations of this Graphics object. (overload 2/2)
helpviewer_keywords: ["Graphics class [GDI+]","TransformPoints method","Graphics.TransformPoints","Graphics::TransformPoints","TransformPoints","TransformPoints method [GDI+]","TransformPoints method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_TransformPoints_destSpace_srcSpace_pts_count_","gdiplus._gdiplus_CLASS_Graphics_TransformPoints_destSpace_srcSpace_pts_count_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_TransformPoints_destSpace_srcSpace_pts_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\transformpoints.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],TransformPoints method, Graphics.TransformPoints, Graphics::TransformPoints, TransformPoints, TransformPoints method [GDI+], TransformPoints method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_TransformPoints_destSpace_srcSpace_pts_count_, gdiplus._gdiplus_CLASS_Graphics_TransformPoints_destSpace_srcSpace_pts_count_
req.header: gdiplusgraphics.h
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
 - Graphics::TransformPoints
 - gdiplusgraphics/Graphics::TransformPoints
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
 - Graphics.TransformPoints
---

# Graphics::TransformPoints


## -description

The <b>Graphics::TransformPoints</b> method converts an array of points from one coordinate space to another. The conversion is based on the current world and page transformations of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -parameters

### -param destSpace [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-coordinatespace">CoordinateSpace</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-coordinatespace">CoordinateSpace</a> enumeration that specifies the destination coordinate space.

### -param srcSpace [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-coordinatespace">CoordinateSpace</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-coordinatespace">CoordinateSpace</a> enumeration that specifies the source coordinate space.

### -param pts [in, out]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to an array that, on input, holds the points to be converted and, on output, holds the converted points.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>pts</i> array.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The world transformation converts points from the world coordinate space to the page coordinate space. The page transformation converts points from the page coordinate space to the device coordinate space. For more information about coordinate spaces, see <a href="/windows/desktop/gdiplus/-gdiplus-types-of-coordinate-systems-about">Types of Coordinate Systems</a>.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object and sets its world transformation to a translation 40 units right and 30 units down. Then the code creates an array of points and passes the address of that array to the <b>Graphics::TransformPoints</b> method of the same <b>Graphics</b> object. The points in the array are transformed by the world transformation of the <b>Graphics</b> object. The code calls the <a href="/previous-versions/ms536020(v=vs.85)">Graphics::DrawLine</a> method twice: once to connect the two points before the transformation and once to connect the two points after the transformation.


```cpp
VOID Example_TransformPoints(HDC hdc)
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));

   // Create an array of two Point objects.
   Point points[2] = {Point(0, 0), Point(100, 50)};

   // Draw a line that connects the two points.
   // No transformation has been performed yet.
   graphics.DrawLine(&pen, points[0], points[1]);

   // Set the world transformation of the Graphics object.
   graphics.TranslateTransform(40.0f, 30.0f);

   // Transform the points in the array from world to page coordinates.
   graphics.TransformPoints(
      CoordinateSpacePage, 
      CoordinateSpaceWorld, 
      points, 
      2);

   // It is the world transformation that takes points from world
   // space to page space. Because the world transformation is a
   // translation 40 to the right and 30 down, the
   // points in the array are now (40, 30) and (140, 80).

   // Draw a line that connects the transformed points.
   graphics.ResetTransform();
   graphics.DrawLine(&pen, points[0], points[1]);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-gettransform">Graphics::GetTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform">Graphics::MultiplyTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-resettransform">Graphics::ResetTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform">Graphics::RotateTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform">Graphics::ScaleTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform">Graphics::SetTransform</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform">Graphics::TranslateTransform</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>



<a href="/windows/desktop/gdiplus/-gdiplus-types-of-coordinate-systems-about">Types of Coordinate Systems</a>
