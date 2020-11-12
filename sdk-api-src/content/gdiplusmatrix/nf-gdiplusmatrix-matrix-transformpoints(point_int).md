---
UID: NF:gdiplusmatrix.Matrix.TransformPoints(Point,INT)
title: Matrix::TransformPoints(IN OUT Point,IN INT) (gdiplusmatrix.h)
description: The Matrix::TransformPoints method multiplies each point in an array by this matrix. Each point is treated as a row matrix. The multiplication is performed with the row matrix on the left and this matrix on the right.
helpviewer_keywords: ["Matrix class [GDI+]","TransformPoints method","Matrix.TransformPoints","Matrix.TransformPoints(IN OUT Point","IN INT)","Matrix.TransformPoints(Point*","INT)","Matrix::TransformPoints","Matrix::TransformPoints(IN OUT Point","IN INT)","TransformPoints","TransformPoints method [GDI+]","TransformPoints method [GDI+]","Matrix class","_gdiplus_CLASS_Matrix_TransformPoints_Point_pts_INT_count_","gdiplus._gdiplus_CLASS_Matrix_TransformPoints_Point_pts_INT_count_"]
old-location: gdiplus\_gdiplus_CLASS_Matrix_TransformPoints_Point_pts_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\matrixtransformpointsmethods\transformpoints_78pointpts_intcount.htm
ms.date: 12/05/2018
ms.keywords: Matrix class [GDI+],TransformPoints method, Matrix.TransformPoints, Matrix.TransformPoints(IN OUT Point,IN INT), Matrix.TransformPoints(Point*,INT), Matrix::TransformPoints, Matrix::TransformPoints(IN OUT Point,IN INT), TransformPoints, TransformPoints method [GDI+], TransformPoints method [GDI+],Matrix class, _gdiplus_CLASS_Matrix_TransformPoints_Point_pts_INT_count_, gdiplus._gdiplus_CLASS_Matrix_TransformPoints_Point_pts_INT_count_
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
 - Matrix::TransformPoints
 - gdiplusmatrix/Matrix::TransformPoints
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
 - Matrix.TransformPoints
---

# Matrix::TransformPoints(IN OUT Point,IN INT)


## -description

The <b>Matrix::TransformPoints</b> method multiplies each point in an array by this matrix. Each point is treated as a row matrix. The multiplication is performed with the row matrix on the left and this matrix on the right.

## -parameters

### -param pts [in, out]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> objects that, on input, contains the points to be transformed and, on output, receives the transformed points. Each point in the array is transformed (multiplied by this matrix) and updated with the result of the transformation.

### -param count [in]

Type: <b>INT</b>

Optional. Integer that specifies the number of points to be transformed. The default value is 1.

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



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>



<a href="/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformpoints(inoutpoint_inint)">TransformPoints Methods</a>



<a href="/windows/desktop/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint)">TransformVectors Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>