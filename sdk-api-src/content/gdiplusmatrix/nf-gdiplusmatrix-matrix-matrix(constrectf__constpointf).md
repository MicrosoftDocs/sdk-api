---
UID: NF:gdiplusmatrix.Matrix.Matrix(constRectF&,constPointF)
title: Matrix::Matrix(IN const RectF &,IN const PointF) (gdiplusmatrix.h)
description: Creates a Matrix::Matrix object based on a rectangle and a point. (overload 1/2)
helpviewer_keywords: ["Matrix","Matrix class [GDI+]","Matrix constructor","Matrix constructor [GDI+]","Matrix constructor [GDI+]","Matrix class","Matrix.Matrix","Matrix.Matrix(IN const RectF &","IN const PointF)","Matrix.Matrix(const RectF&","const PointF*)","Matrix::Matrix","Matrix::Matrix(IN const RectF &","IN const PointF)","_gdiplus_CLASS_Matrix_Matrix_RectF_rect_PointF_dstplg_","gdiplus._gdiplus_CLASS_Matrix_Matrix_RectF_rect_PointF_dstplg_"]
old-location: gdiplus\_gdiplus_CLASS_Matrix_Matrix_RectF_rect_PointF_dstplg_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixconstructors\matrix_21rectfamprect_pointfdstplg.htm
ms.date: 12/05/2018
ms.keywords: Matrix, Matrix class [GDI+],Matrix constructor, Matrix constructor [GDI+], Matrix constructor [GDI+],Matrix class, Matrix.Matrix, Matrix.Matrix(IN const RectF &,IN const PointF), Matrix.Matrix(const RectF&,const PointF*), Matrix::Matrix, Matrix::Matrix(IN const RectF &,IN const PointF), _gdiplus_CLASS_Matrix_Matrix_RectF_rect_PointF_dstplg_, gdiplus._gdiplus_CLASS_Matrix_Matrix_RectF_rect_PointF_dstplg_
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

# Matrix::Matrix(IN const RectF &,IN const PointF)


## -description

Creates a <b>Matrix::Matrix</b> object based on a rectangle and a point.

## -parameters

### -param rect [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a></b>

Reference to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a> object. The <b>X</b> data member of the rectangle specifies the matrix element in row 1, column 1. The <b>Y</b> data member of the rectangle specifies the matrix element in row 1, column 2. The <b>Width</b> data member of the rectangle specifies the matrix element in row 2, column 1. The <b>Height</b> data member of the rectangle specifies the matrix element in row 2, column 2.

### -param dstplg [in]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> object. The <b>X</b> data member of the point specifies the matrix element in row 3, column 1. The <b>Y</b> data member of the point specifies the matrix element in row 3, column 2.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-global-and-local-transformations-about">Global and Local Transformations</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-class-matrix-constructors">Matrix Constructors</a>



<a href="/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>
