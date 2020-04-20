---
UID: NF:gdiplusmatrix.Matrix.Shear
title: Matrix::Shear (gdiplusmatrix.h)
description: The Matrix::Shear method updates this matrix with the product of itself and a shearing matrix.helpviewer_keywords: ["Matrix class [GDI+]","Shear method","Matrix.Shear","Matrix::Shear","Shear","Shear method [GDI+]","Shear method [GDI+]","Matrix class","_gdiplus_CLASS_Matrix_Shear_shearX_shearY_order_","gdiplus._gdiplus_CLASS_Matrix_Shear_shearX_shearY_order_"]
old-location: gdiplus\_gdiplus_CLASS_Matrix_Shear_shearX_shearY_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\shear.htm
ms.date: 12/05/2018
ms.keywords: Matrix class [GDI+],Shear method, Matrix.Shear, Matrix::Shear, Shear, Shear method [GDI+], Shear method [GDI+],Matrix class, _gdiplus_CLASS_Matrix_Shear_shearX_shearY_order_, gdiplus._gdiplus_CLASS_Matrix_Shear_shearX_shearY_order_
f1_keywords:
- gdiplusmatrix/Matrix.Shear
dev_langs:
- c++
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
- Matrix.Shear
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Matrix::Shear


## -description


The <b>Matrix::Shear</b> method updates this matrix with the product of itself and a shearing matrix.


## -parameters




### -param shearX [in]

Type: <b>REAL</b>

Real number that specifies the horizontal shear factor. 


### -param shearY [in]

Type: <b>REAL</b>

Real number that specifies the vertical shear factor. 


### -param order [in]

Type: <b>REAL</b>

Optional. Element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a> enumeration that specifies the order of the multiplication. MatrixOrderPrepend specifies that the shearing matrix is on the left, and MatrixOrderAppend specifies that the shearing matrix is on the right. The default value is MatrixOrderPrepend. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the Status enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-global-and-local-transformations-about">Global and Local Transformations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply">Matrix::Multiply</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate">Matrix::Rotate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat">Matrix::RotateAt</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-scale">Matrix::Scale</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-translate">Matrix::Translate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>
 

 

