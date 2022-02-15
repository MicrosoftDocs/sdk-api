---
UID: NF:gdiplusmatrix.Matrix.Invert
title: Matrix::Invert (gdiplusmatrix.h)
description: If this matrix is invertible, the Matrix::Invert method replaces the elements of this matrix with the elements of its inverse.
helpviewer_keywords: ["Invert","Invert method [GDI+]","Invert method [GDI+]","Matrix class","Matrix class [GDI+]","Invert method","Matrix.Invert","Matrix::Invert","_gdiplus_CLASS_Matrix_Invert_","gdiplus._gdiplus_CLASS_Matrix_Invert_"]
old-location: gdiplus\_gdiplus_CLASS_Matrix_Invert_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\invert.htm
ms.date: 12/05/2018
ms.keywords: Invert, Invert method [GDI+], Invert method [GDI+],Matrix class, Matrix class [GDI+],Invert method, Matrix.Invert, Matrix::Invert, _gdiplus_CLASS_Matrix_Invert_, gdiplus._gdiplus_CLASS_Matrix_Invert_
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
 - Matrix::Invert
 - gdiplusmatrix/Matrix::Invert
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
 - Matrix.Invert
---

# Matrix::Invert


## -description

If this matrix is invertible, the <b>Matrix::Invert</b> method replaces the elements of this matrix with the elements of its inverse.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

If this matrix is not invertible, the method fails and returns InvalidParameter.


#### Examples



The following example passes the address of a 
						<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object to the 
						<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform">SetTransform</a> method of a 
						<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object and then draws a rectangle. The rectangle is translated 30 units right and 20 units down by the world transformation of the 
						<b>Graphics</b> object. The code calls the <b>Matrix::Invert</b> method of the 
						<b>Matrix</b> object and sets the world transformation of the 
						<b>Graphics</b> object to the inverted matrix. The code draws a second rectangle that is translated 30 units left and 20 units up.


```cpp
VOID Example_Invert(HDC hdc)
{
   Graphics myGraphics(hdc);
   Pen myPen(Color(255, 0, 0, 255));

   Matrix matrix(1.0f, 0.0f, 0.0f, 1.0f, 30.0f, 20.0f);

   myGraphics.SetTransform(&matrix);
   myGraphics.DrawRectangle(&myPen, 0, 0, 200, 100);
   matrix.Invert();
   myGraphics.SetTransform(&matrix);
   myGraphics.DrawRectangle(&myPen, 0, 0, 200, 100);  
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-global-and-local-transformations-about">Global and Local Transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible">Matrix::IsInvertible</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>
