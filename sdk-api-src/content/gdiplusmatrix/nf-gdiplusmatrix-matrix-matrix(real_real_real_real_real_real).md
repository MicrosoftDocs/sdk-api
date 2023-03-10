---
UID: NF:gdiplusmatrix.Matrix.Matrix(REAL,REAL,REAL,REAL,REAL,REAL)
title: Matrix::Matrix(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL) (gdiplusmatrix.h)
description: Creates and initializes a Matrix::Matrix object based on six numbers that define an affine transformation.
helpviewer_keywords: ["Matrix","Matrix class [GDI+]","Matrix constructor","Matrix constructor [GDI+]","Matrix constructor [GDI+]","Matrix class","Matrix.Matrix","Matrix.Matrix(IN REAL","IN REAL","IN REAL","IN REAL","IN REAL","IN REAL)","Matrix.Matrix(REAL","REAL","REAL","REAL","REAL","REAL)","Matrix::Matrix","Matrix::Matrix(IN REAL","IN REAL","IN REAL","IN REAL","IN REAL","IN REAL)","_gdiplus_CLASS_Matrix_Matrix_m11_m12_m21_m22_dx_dy_","gdiplus._gdiplus_CLASS_Matrix_Matrix_m11_m12_m21_m22_dx_dy_"]
old-location: gdiplus\_gdiplus_CLASS_Matrix_Matrix_m11_m12_m21_m22_dx_dy_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixconstructors\matrix_67m11_m12_m21_m22_dx_dy.htm
ms.date: 12/05/2018
ms.keywords: Matrix, Matrix class [GDI+],Matrix constructor, Matrix constructor [GDI+], Matrix constructor [GDI+],Matrix class, Matrix.Matrix, Matrix.Matrix(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), Matrix.Matrix(REAL,REAL,REAL,REAL,REAL,REAL), Matrix::Matrix, Matrix::Matrix(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), _gdiplus_CLASS_Matrix_Matrix_m11_m12_m21_m22_dx_dy_, gdiplus._gdiplus_CLASS_Matrix_Matrix_m11_m12_m21_m22_dx_dy_
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
 - Matrix::Matrix
 - gdiplusmatrix/Matrix::Matrix
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
 - Matrix.Matrix
---

# Matrix::Matrix(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)


## -description

Creates and initializes a <b>Matrix::Matrix</b> object based on six numbers that define an affine transformation.

## -parameters

### -param m11 [in]

Type: <b>REAL</b>

Real number that specifies the element in the first row, first column&mdash;horizontal scaling component or cosine of rotation angle.

### -param m12 [in]

Type: <b>REAL</b>

Real number that specifies the element in the first row, second column&mdash;horizontal shear component or sine of rotation angle.

### -param m21 [in]

Type: <b>REAL</b>

Real number that specifies the element in the second row, first column&mdash;vertical shear component or negative sine of rotation angle.

### -param m22 [in]

Type: <b>REAL</b>

Real number that specifies the element in the second row, second column&mdash;vertical scaling component or cosine of rotation angle.

### -param dx [in]

Type: <b>REAL</b>

Real number that specifies the element in the third row, first column&mdash;horizontal translation component.

### -param dy [in]

Type: <b>REAL</b>

Real number that specifies the element in the third row, second column&mdash;vertical translation component.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-global-and-local-transformations-about">Global and Local Transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-class-matrix-constructors">Matrix Constructors</a>



<a href="/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>
