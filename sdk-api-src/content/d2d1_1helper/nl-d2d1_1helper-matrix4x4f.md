---
UID: NL:d2d1_1helper.Matrix4x4F
title: Matrix4x4F (d2d1_1helper.h)
author: windows-sdk-content
description: The Matrix4x4F class represents a 4-by-4 matrix and provides convenience methods for creating matrices.
old-location: direct2d\matrix4x4f.htm
tech.root: Direct2D
ms.assetid: 113861DF-2E6D-4930-82DC-AA592882E21C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Matrix4x4F, Matrix4x4F class [Direct2D], Matrix4x4F class [Direct2D],described, d2d1_1helper/Matrix4x4F, direct2d.matrix4x4f
ms.topic: class
f1_keywords: 
 - "d2d1_1helper/Matrix4x4F"
req.header: d2d1_1helper.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1_1helper.h
api_name:
 - Matrix4x4F
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Matrix4x4F class


## -description


The <b>Matrix4x4F</b> class represents a 4-by-4 matrix and provides convenience methods for creating matrices.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">Matrix4x4F</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/windows/win32/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-operator-mult">Operators</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>Matrix4x4F</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-determinant">Determinant</a>
</td>
<td align="left" width="63%">
Calculates the determinant of the matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-isidentity">IsIdentity</a>
</td>
<td align="left" width="63%">
Indicates whether this matrix is the identity matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-perspectiveprojection">PerspectiveProjection</a>
</td>
<td align="left" width="63%">
A perspective transformation given a depth value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-reinterpretbasetype(d2d1_matrix_4x4_f)">ReinterpretBaseType</a>
</td>
<td align="left" width="63%">
Converts the specified <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh848012(v=vs.85)">ReinterpretBaseType(const D2D1_MATRIX_4X4_F *pMatrix)</a>
</td>
<td align="left" width="63%">
Converts the specified <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-rotationarbitraryaxis">RotationArbitraryAxis</a>
</td>
<td align="left" width="63%">
Determines the 3-D Rotation matrix for an arbitrary axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-rotationx">RotationX</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the X axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-rotationy">RotationY</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the Y axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-rotationz">RotationZ</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the Z axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-scale">Scale</a>
</td>
<td align="left" width="63%">
Scales the perspective plane of the matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-setproduct">SetProduct</a>
</td>
<td align="left" width="63%">
Multiplies the two matrices and stores the result in this matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-skewx">SkewX</a>
</td>
<td align="left" width="63%">
Skews the matrix in the X direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-skewy">SkewY</a>
</td>
<td align="left" width="63%">
Skews the matrix in the Y direction.

</td>
</tr>
</table> 
<h3><a id="operators"></a>Operators</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Matrix4x4F</b> class has these operators.
<table>
<tr>
<th align="left" width="37%">Operator</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-operator-mult">operator*</a>
</td>
<td align="left" width="63%">
Multiplies this matrix with the specified matrix and returns the result.

</td>
</tr>
</table> 


## -members

The <b>Matrix4x4F</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-determinant">Determinant</a>
</td>
<td align="left" width="63%">
Calculates the determinant of the matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-isidentity">IsIdentity</a>
</td>
<td align="left" width="63%">
Indicates whether this matrix is the identity matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-perspectiveprojection">PerspectiveProjection</a>
</td>
<td align="left" width="63%">
A perspective transformation given a depth value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-reinterpretbasetype(d2d1_matrix_4x4_f)">ReinterpretBaseType</a>
</td>
<td align="left" width="63%">
Converts the specified <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh848012(v=vs.85)">ReinterpretBaseType(const D2D1_MATRIX_4X4_F *pMatrix)</a>
</td>
<td align="left" width="63%">
Converts the specified <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-rotationarbitraryaxis">RotationArbitraryAxis</a>
</td>
<td align="left" width="63%">
Determines the 3-D Rotation matrix for an arbitrary axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-rotationx">RotationX</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the X axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-rotationy">RotationY</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the Y axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-rotationz">RotationZ</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the Z axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-scale">Scale</a>
</td>
<td align="left" width="63%">
Scales the perspective plane of the matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-setproduct">SetProduct</a>
</td>
<td align="left" width="63%">
Multiplies the two matrices and stores the result in this matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-skewx">SkewX</a>
</td>
<td align="left" width="63%">
Skews the matrix in the X direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-skewy">SkewY</a>
</td>
<td align="left" width="63%">
Skews the matrix in the Y direction.

</td>
</tr>
</table>Calculates the determinant of the matrix.

Indicates whether this matrix is the identity matrix.

A perspective transformation given a depth value.

Converts the specified <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

Converts the specified <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

Determines the 3-D Rotation matrix for an arbitrary axis.

Rotates the transform matrix around the X axis.

Rotates the transform matrix around the Y axis.

Rotates the transform matrix around the Z axis.

Scales the perspective plane of the matrix.

Multiplies the two matrices and stores the result in this matrix.

Skews the matrix in the X direction.

Skews the matrix in the Y direction.

 

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Matrix4x4F</b> class has these operators.
<table>
<tr>
<th align="left" width="37%">Operator</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/d2d1_1helper/nf-d2d1_1helper-matrix4x4f-operator-mult">operator*</a>
</td>
<td align="left" width="63%">
Multiplies this matrix with the specified matrix and returns the result.

</td>
</tr>
</table>Multiplies this matrix with the specified matrix and returns the result.

 

