---
UID: NF:gdiplusmatrix.Matrix.TransformVectors(Point,INT)
title: Matrix::TransformVectors(IN OUT Point,IN INT) (gdiplusmatrix.h)
description: The Matrix::TransformVectors method multiplies each vector in an array by this matrix.
helpviewer_keywords: ["Matrix class [GDI+]","TransformVectors method","Matrix.TransformVectors","Matrix.TransformVectors(IN OUT Point","IN INT)","Matrix.TransformVectors(Point*","INT)","Matrix::TransformVectors","Matrix::TransformVectors(IN OUT Point","IN INT)","TransformVectors","TransformVectors method [GDI+]","TransformVectors method [GDI+]","Matrix class","_gdiplus_CLASS_Matrix_TransformVectors_Point_pts_INT_count_","gdiplus._gdiplus_CLASS_Matrix_TransformVectors_Point_pts_INT_count_"]
old-location: gdiplus\_gdiplus_CLASS_Matrix_TransformVectors_Point_pts_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\matrixtransformvectorsmethods\transformvectors.htm
ms.date: 12/05/2018
ms.keywords: Matrix class [GDI+],TransformVectors method, Matrix.TransformVectors, Matrix.TransformVectors(IN OUT Point,IN INT), Matrix.TransformVectors(Point*,INT), Matrix::TransformVectors, Matrix::TransformVectors(IN OUT Point,IN INT), TransformVectors, TransformVectors method [GDI+], TransformVectors method [GDI+],Matrix class, _gdiplus_CLASS_Matrix_TransformVectors_Point_pts_INT_count_, gdiplus._gdiplus_CLASS_Matrix_TransformVectors_Point_pts_INT_count_
req.header: gdiplusmatrix.h
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
 - Matrix::TransformVectors
 - gdiplusmatrix/Matrix::TransformVectors
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
 - Matrix.TransformVectors
---

# Matrix::TransformVectors(IN OUT Point,IN INT)


## -description

The <b>Matrix::TransformVectors</b> method multiplies each vector in an array by this matrix. The translation elements of this matrix (third row) are ignored. Each vector is treated as a row matrix. The multiplication is performed with the row matrix on the left and this matrix on the right.

## -parameters

### -param pts [in, out]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> objects that, on input, contains the vectors to be transformed and, on output, receives the transformed vectors. Each vector in the array is transformed (multiplied by this matrix) and updated with the result of the transformation.

### -param count [in]

Type: <b>INT</b>

Optional. Integer that specifies the number of vectors to be transformed. The default value is 1.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

While a point represents position, a vector represents an entity (for example, velocity or acceleration) that has a direction and a magnitude. Thus, the endpoints of a line segment are points, but their difference is a vector—the length and direction of that line segment.

Vectors are similar to points in many ways. Like points, they are represented by x- and y-coordinates, so GDI+ uses the same classes (<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> and 
				<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>) to represent vectors as it uses to represent points. The subtle difference between vectors and points is the way they are affected by transformations. In the physical world, moving the origin of the coordinate system changes the coordinates of all position points, but it will not alter any velocity vectors. Vectors can be scaled, rotated, sheared or flipped, but not translated (moved). Thus, when an affine transformation is applied to a vector, the translation component (the last row of the matrix) is ignored.


#### Examples



The following example creates a vector and a point. The tip of the vector and the point are at the same location: (100, 50). The code creates a 
						<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object and initializes its elements so that it represents a clockwise rotation followed by a translation 100 units to the right. The code calls the 
						<a href="/previous-versions/ms535321(v=vs.85)">Matrix::TransformPoints</a> method of the matrix to transform the point and calls the <b>Matrix::TransformVectors</b> method of the matrix to transform the vector. The entire transformation (rotation followed by translation) is performed on the point, but only the rotation part of the transformation is performed on the vector. The elements of the matrix that represent translation are ignored by the <b>Matrix::TransformVectors</b> method.


```cpp
VOID Example_TransVectors(HDC hdc)
{
   Graphics graphics(hdc);

   Pen pen(Color(255, 0, 0, 255), 7);
   pen.SetEndCap(LineCapArrowAnchor);
   SolidBrush brush(Color(255, 0, 0, 255));

   // A point and a vector, same representation but different behavior
   Point point(100, 50);
   Point vector(100, 50);

   // Draw the original point and vector in blue.
   graphics.FillEllipse(&brush, point.X - 5, point.Y - 5, 10, 10);

   graphics.DrawLine(&pen, Point(0, 0), vector);

   // Transform.
   Matrix matrix(0.8f, 0.6f, -0.6f, 0.8f, 100.0f, 0.0f);
   matrix.TransformPoints(&point);
   matrix.TransformVectors(&vector);

   // Draw the transformed point and vector in red.
   pen.SetColor(Color(255, 255, 0, 0));
   brush.SetColor(Color(255, 255, 0, 0));
   graphics.FillEllipse(&brush, point.X - 5, point.Y - 5, 10, 10);
   graphics.DrawLine(&pen, Point(0, 0), vector); 
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-global-and-local-transformations-about">Global and Local Transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>



<a href="/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformpoints(inoutpoint_inint)">TransformPoints Methods</a>



<a href="/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint)">TransformVectors Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>