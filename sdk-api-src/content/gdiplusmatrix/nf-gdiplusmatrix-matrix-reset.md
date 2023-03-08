---
UID: NF:gdiplusmatrix.Matrix.Reset
title: Matrix::Reset (gdiplusmatrix.h)
description: The Matrix::Reset method updates this matrix with the elements of the identity matrix.
helpviewer_keywords: ["Matrix class [GDI+]","Reset method","Matrix.Reset","Matrix::Reset","Reset","Reset method [GDI+]","Reset method [GDI+]","Matrix class","_gdiplus_CLASS_Matrix_Reset_","gdiplus._gdiplus_CLASS_Matrix_Reset_"]
old-location: gdiplus\_gdiplus_CLASS_Matrix_Reset_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\reset_41.htm
ms.date: 12/05/2018
ms.keywords: Matrix class [GDI+],Reset method, Matrix.Reset, Matrix::Reset, Reset, Reset method [GDI+], Reset method [GDI+],Matrix class, _gdiplus_CLASS_Matrix_Reset_, gdiplus._gdiplus_CLASS_Matrix_Reset_
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
 - Matrix::Reset
 - gdiplusmatrix/Matrix::Reset
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
 - Matrix.Reset
---

# Matrix::Reset


## -description

The <b>Matrix::Reset</b> method updates this matrix with the elements of the identity matrix.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The elements on the main diagonal of the identity matrix are 1. All other elements of the identity matrix are 0.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that represents a horizontal scaling by a factor of 5 and a vertical scaling by a factor of 3. The code calls the <b>Matrix::Reset</b> method to replace the elements of that matrix with the elements of the identity matrix. Then the code calls the 
						<a href="/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-translate">Matrix::Translate</a> method to update the matrix with the product of itself (the identity) and a translation matrix. The result is that the matrix represents only the translation, not the scaling. The code uses the matrix to set the world transformation of a 
						<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object and then draws a rectangle that is transformed according to that world transformation.


```cpp
VOID Example_Reset(HDC hdc)
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));

   Matrix matrix(5.0f, 0.0f, 0.0f, 3.0f, 0.0f, 0.0f);
   matrix.Reset();
   matrix.Translate(50.0f, 40.0f);

   graphics.SetTransform(&matrix);
   graphics.DrawRectangle(&pen, 0, 0, 100, 100);  
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-global-and-local-transformations-about">Global and Local Transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-isidentity">Matrix::IsIdentity</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>
