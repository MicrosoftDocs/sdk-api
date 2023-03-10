---
UID: NF:gdiplusmatrix.Matrix.TransformVectors(PointF,INT)
title: Matrix::TransformVectors (gdiplusmatrix.h)
description: This topic lists the TransformVectors methods of the Matrix class. For a complete list of methods for the Matrix class, see Matrix Methods.
helpviewer_keywords: ["Matrix.TransformVectors","Matrix::TransformVectors","TransformVectors","TransformVectors methods [GDI+]","_gdiplus_CLASS_Matrix_TransformVectors_Methods","gdiplus._gdiplus_CLASS_Matrix_TransformVectors_Methods","gdiplusmatrix/TransformVectors"]
old-location: gdiplus\_gdiplus_CLASS_Matrix_TransformVectors_Methods.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\matrixtransformvectorsmethods.htm
ms.date: 12/05/2018
ms.keywords: Matrix.TransformVectors, Matrix::TransformVectors, TransformVectors, TransformVectors methods [GDI+], _gdiplus_CLASS_Matrix_TransformVectors_Methods, gdiplus._gdiplus_CLASS_Matrix_TransformVectors_Methods, gdiplusmatrix/TransformVectors
req.header: gdiplusmatrix.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
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
 - HeaderDef
api_location:
 - gdiplusmatrix.h
api_name:
 - Matrix.TransformVectors
---

# Matrix::TransformVectors


## -description

<span>This topic lists the TransformVectors methods of the <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> class. For a complete list of methods for the <b>Matrix</b> class, see <a href="/windows/desktop/gdiplus/-gdiplus-class-matrix-methods">Matrix Methods</a>. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms535318(v=vs.85)">TransformVectors(Point*,INT)</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/ms535318(v=vs.85)">Matrix::TransformVectors</a> method multiplies each vector in an array by this matrix. The translation elements of this matrix (third row) are ignored. Each vector is treated as a row matrix. The multiplication is performed with the row matrix on the left and this matrix on the right.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms535319(v=vs.85)">TransformVectors(PointF*,INT)</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/ms535319(v=vs.85)">Matrix::TransformVectors</a> method multiplies each vector in an array by this matrix. The translation elements of this matrix (third row) are ignored. Each vector is treated as a row matrix. The multiplication is performed with the row matrix on the left and this matrix on the right.

</td>
</tr>
</table>

## -parameters