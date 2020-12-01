---
UID: NF:gdiplusmatrix.Matrix.SetElements
title: Matrix::SetElements (gdiplusmatrix.h)
description: The Matrix::SetElements method sets the elements of this matrix.
helpviewer_keywords: ["Matrix class [GDI+]","SetElements method","Matrix.SetElements","Matrix::SetElements","SetElements","SetElements method [GDI+]","SetElements method [GDI+]","Matrix class","_gdiplus_CLASS_Matrix_SetElements_m11_m12_m21_m22_dx_dy_","gdiplus._gdiplus_CLASS_Matrix_SetElements_m11_m12_m21_m22_dx_dy_"]
old-location: gdiplus\_gdiplus_CLASS_Matrix_SetElements_m11_m12_m21_m22_dx_dy_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\setelements.htm
ms.date: 12/05/2018
ms.keywords: Matrix class [GDI+],SetElements method, Matrix.SetElements, Matrix::SetElements, SetElements, SetElements method [GDI+], SetElements method [GDI+],Matrix class, _gdiplus_CLASS_Matrix_SetElements_m11_m12_m21_m22_dx_dy_, gdiplus._gdiplus_CLASS_Matrix_SetElements_m11_m12_m21_m22_dx_dy_
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
 - Matrix::SetElements
 - gdiplusmatrix/Matrix::SetElements
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
 - Matrix.SetElements
---

# Matrix::SetElements


## -description

The <b>Matrix::SetElements</b> method sets the elements of this matrix.

## -parameters

### -param m11 [in]

Type: <b>REAL</b>

Real number that specifies the element in the first row, first column.

### -param m12 [in]

Type: <b>REAL</b>

Real number that specifies the element in the first row, second column.

### -param m21 [in]

Type: <b>REAL</b>

Real number that specifies the element in the second row, first column.

### -param m22 [in]

Type: <b>REAL</b>

Real number that specifies the element in the second row, second column.

### -param dx [in]

Type: <b>REAL</b>

Real number that specifies the element in the third row, first column.

### -param dy [in]

Type: <b>REAL</b>

Real number that specifies the element in the third row, second column.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-global-and-local-transformations-about">Global and Local Transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-getelements">Matrix::GetElements</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>