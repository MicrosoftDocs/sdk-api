---
UID: NF:gdiplusmatrix.Matrix.TransformVectors(IN OUT Point,IN INT)
title: Matrix::TransformVectors(IN OUT Point,IN INT)
author: windows-sdk-content
description: This topic lists the TransformVectors methods of the Matrix class. For a complete list of methods for the Matrix class, see Matrix Methods.
old-location: gdiplus\_gdiplus_CLASS_Matrix_TransformVectors_Methods.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\matrixtransformvectorsmethods.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Matrix.TransformVectors, Matrix.TransformVectors(IN OUT Point,IN INT), Matrix::TransformVectors, Matrix::TransformVectors(IN OUT Point,IN INT), TransformVectors, TransformVectors methods [GDI+], _gdiplus_CLASS_Matrix_TransformVectors_Methods, gdiplus._gdiplus_CLASS_Matrix_TransformVectors_Methods, gdiplusmatrix/TransformVectors
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	gdiplusmatrix.h
api_name:
-	Matrix.TransformVectors
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# Matrix::TransformVectors(IN OUT Point,IN INT)


## -description


<span>This topic lists the TransformVectors methods of the <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> class. For a complete list of methods for the <b>Matrix</b> class, see <a href="https://msdn.microsoft.com/d43a7956-9822-4093-9722-91f0d2edf50c">Matrix Methods</a>. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c44b813-9045-4452-8598-87f119ad2870">TransformVectors(Point*,INT)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/6c44b813-9045-4452-8598-87f119ad2870">Matrix::TransformVectors</a> method multiplies each vector in an array by this matrix. The translation elements of this matrix (third row) are ignored. Each vector is treated as a row matrix. The multiplication is performed with the row matrix on the left and this matrix on the right.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3afb707-e507-4d6f-a8e0-42c7fa559f3e">TransformVectors(PointF*,INT)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/a3afb707-e507-4d6f-a8e0-42c7fa559f3e">Matrix::TransformVectors</a> method multiplies each vector in an array by this matrix. The translation elements of this matrix (third row) are ignored. Each vector is treated as a row matrix. The multiplication is performed with the row matrix on the left and this matrix on the right.

</td>
</tr>
</table>

## -parameters

