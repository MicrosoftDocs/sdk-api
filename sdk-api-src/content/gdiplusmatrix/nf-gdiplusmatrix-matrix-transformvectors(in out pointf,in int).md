---
UID: NF:gdiplusmatrix.Matrix.TransformVectors(IN OUT PointF,IN INT)
title: Matrix::TransformVectors(IN OUT PointF,IN INT)
author: windows-sdk-content
description: The Matrix::TransformVectors method multiplies each vector in an array by this matrix.
old-location: gdiplus\_gdiplus_CLASS_Matrix_TransformVectors_PointF_pts_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\matrixtransformvectorsmethods\transformvectors_2pointfpts_intcount.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: Matrix class [GDI+],TransformVectors method, Matrix.TransformVectors, Matrix.TransformVectors(IN OUT PointF,IN INT), Matrix.TransformVectors(PointF*,INT), Matrix::TransformVectors, Matrix::TransformVectors(IN OUT PointF,IN INT), TransformVectors, TransformVectors method [GDI+], TransformVectors method [GDI+],Matrix class, _gdiplus_CLASS_Matrix_TransformVectors_PointF_pts_INT_count_, gdiplus._gdiplus_CLASS_Matrix_TransformVectors_PointF_pts_INT_count_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Matrix.TransformVectors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Matrix::TransformVectors(IN OUT PointF,IN INT)


## -description


The <b>Matrix::TransformVectors</b> method multiplies each vector in an array by this matrix. The translation elements of this matrix (third row) are ignored. Each vector is treated as a row matrix. The multiplication is performed with the row matrix on the left and this matrix on the right.


## -parameters




### -param pts [in, out]

Type: <b><a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a> objects that, on input, contains the vectors to be transformed and, on output, receives the transformed vectors. Each vector in the array is transformed (multiplied by this matrix) and updated with the result of the transformation. 


### -param count [in]

Type: <b>INT</b>

Optional. Integer that specifies the number of points to be transformed. The default value is 1. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



While a point represents position, a vector represents an entity (for example, velocity or acceleration) that has a direction and a magnitude. Thus, the endpoints of a line segment are points, but their difference is a vector—the length and direction of that line segment.

Vectors are similar to points in many ways. Like points, they are represented by x- and y-coordinates, so GDI+ uses the same classes (
				<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a> and <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>) to represent vectors as it uses to represent points. The subtle difference between vectors and points is the way they are affected by transformations. In the physical world, moving the origin of the coordinate system changes the coordinates of all position points, but it will not alter any velocity vectors. Vectors can be scaled, rotated, sheared or flipped, but not translated (moved). Thus, when an affine transformation is applied to a vector, the translation component (the last row of the matrix) is ignored.


#### Examples



The following example creates a vector and a point. The tip of the vector and the point are at the same location: (100, 50). The code creates a 
						<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object and initializes its elements so that it represents a clockwise rotation followed by a translation 100 units to the right. The code calls the 
						<a href="https://msdn.microsoft.com/a290aa79-64a0-440e-bfec-a8e66057ec14">TransformPoints Methods</a> method of the matrix to transform the point and calls the <b>Matrix::TransformVectors</b> method of the matrix to transform the vector. The entire transformation (rotation followed by translation) is performed on the point, but only the rotation part of the transformation is performed on the vector. The elements of the matrix that represent translation are ignored by the <b>Matrix::TransformVectors</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_TransVectorsF(HDC hdc)
{
   Graphics graphics(hdc);

   Pen pen(Color(255, 0, 0, 255), 7);
   pen.SetEndCap(LineCapArrowAnchor);
   SolidBrush brush(Color(255, 0, 0, 255));

   // A point and a vector, same representation but different behavior
   PointF point(100.0f, 50.0f);
   PointF vector(100.0f, 50.0f);

   // Draw the original point and vector in blue.
   graphics.FillEllipse(&amp;brush, point.X - 5.0f, point.Y - 5.0f, 10.0f, 10.0f);

   graphics.DrawLine(&amp;pen, PointF(0.0f, 0.0f), vector);

   // Transform.
   Matrix matrix(0.8f, 0.6f, -0.6f, 0.8f, 100.0f, 0.0f);
   matrix.TransformPoints(&amp;point);
   matrix.TransformVectors(&amp;vector);

   // Draw the transformed point and vector in red.
   pen.SetColor(Color(255, 255, 0, 0));
   brush.SetColor(Color(255, 255, 0, 0));
   graphics.FillEllipse(&amp;brush, point.X - 5.0f, point.Y - 5.0f, 10.0f, 10.0f);
   graphics.DrawLine(&amp;pen, PointF(0.0f, 0.0f), vector);  
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9f744c2a-f1f3-4a7e-ab0c-37aa1df01623">Global and Local Transformations</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/62215ae0-b095-42b2-911c-aa7607a8b61a">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>



<a href="https://msdn.microsoft.com/a290aa79-64a0-440e-bfec-a8e66057ec14">TransformPoints Methods</a>



<a href="https://msdn.microsoft.com/6a2ed6a7-825a-422b-b035-b88746f3ab5d">TransformVectors Methods</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

