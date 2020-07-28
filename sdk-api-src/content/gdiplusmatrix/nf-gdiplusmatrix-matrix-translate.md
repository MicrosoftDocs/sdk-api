---
UID: NF:gdiplusmatrix.Matrix.Translate
title: Matrix::Translate (gdiplusmatrix.h)
description: The Matrix::Translate method updates this matrix with the product of itself and a translation matrix.
helpviewer_keywords: ["Matrix class [GDI+]","Translate method","Matrix.Translate","Matrix::Translate","Translate","Translate method [GDI+]","Translate method [GDI+]","Matrix class","_gdiplus_CLASS_Matrix_Translate_offsetX_offsetY_order_","gdiplus._gdiplus_CLASS_Matrix_Translate_offsetX_offsetY_order_"]
old-location: gdiplus\_gdiplus_CLASS_Matrix_Translate_offsetX_offsetY_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\translate.htm
ms.date: 12/05/2018
ms.keywords: Matrix class [GDI+],Translate method, Matrix.Translate, Matrix::Translate, Translate, Translate method [GDI+], Translate method [GDI+],Matrix class, _gdiplus_CLASS_Matrix_Translate_offsetX_offsetY_order_, gdiplus._gdiplus_CLASS_Matrix_Translate_offsetX_offsetY_order_
f1_keywords:
- gdiplusmatrix/Matrix.Translate
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
- Matrix.Translate
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Matrix::Translate


## -description


The <b>Matrix::Translate</b> method updates this matrix with the product of itself and a translation matrix.


## -parameters




### -param offsetX [in]

Type: <b>REAL</b>

Real number that specifies the horizontal component of the translation. 


### -param offsetY [in]

Type: <b>REAL</b>

Real number that specifies the vertical component of the translation. 


### -param order [in]

Type: <b>REAL</b>

Optional. Element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a> enumeration that specifies the order of the multiplication. MatrixOrderPrepend specifies that the translation matrix is on the left, and MatrixOrderAppend specifies that the translation matrix is on the right. The default value is MatrixOrderPrepend. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-global-and-local-transformations-about">Global and Local Transformations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply">Matrix::Multiply</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate">Matrix::Rotate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat">Matrix::RotateAt</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-scale">Matrix::Scale</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-shear">Matrix::Shear</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-matrixorder">MatrixOrder</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>
 

 

