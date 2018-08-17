---
UID: NL:d2d1_1helper.Matrix4x4F
title: Matrix4x4F
author: windows-sdk-content
description: The Matrix4x4F class represents a 4-by-4 matrix and provides convenience methods for creating matrices.
old-location: direct2d\matrix4x4f.htm
old-project: direct2d
ms.assetid: 113861DF-2E6D-4930-82DC-AA592882E21C
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Matrix4x4F, Matrix4x4F class [Direct2D], Matrix4x4F class [Direct2D],described, d2d1_1helper/Matrix4x4F, direct2d.matrix4x4f
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: d2d1_1helper.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D1_STROKE_STYLE_PROPERTIES1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1_1helper.h
api_name:
 - Matrix4x4F
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# Matrix4x4F class


## -description


The <b>Matrix4x4F</b> class represents a 4-by-4 matrix and provides convenience methods for creating matrices.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">Matrix4x4F</b> has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Operators</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>Matrix4x4F</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848007(v=VS.85).aspx">Determinant</a>
</td>
<td align="left" width="63%">
Calculates the determinant of the matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848008(v=VS.85).aspx">IsIdentity</a>
</td>
<td align="left" width="63%">
Indicates whether this matrix is the identity matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848010(v=VS.85).aspx">PerspectiveProjection</a>
</td>
<td align="left" width="63%">
A perspective transformation given a depth value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848011(v=VS.85).aspx">ReinterpretBaseType</a>
</td>
<td align="left" width="63%">
Converts the specified <a href="https://msdn.microsoft.com/en-us/library/Dd368132(v=VS.85).aspx">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/204EF85B-BDD4-4A54-96DB-39421F36A75C">ReinterpretBaseType(const D2D1_MATRIX_4X4_F *pMatrix)</a>
</td>
<td align="left" width="63%">
Converts the specified <a href="https://msdn.microsoft.com/en-us/library/Dd368132(v=VS.85).aspx">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848013(v=VS.85).aspx">RotationArbitraryAxis</a>
</td>
<td align="left" width="63%">
Determines the 3-D Rotation matrix for an arbitrary axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848014(v=VS.85).aspx">RotationX</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the X axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848015(v=VS.85).aspx">RotationY</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the Y axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848016(v=VS.85).aspx">RotationZ</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the Z axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848017(v=VS.85).aspx">Scale</a>
</td>
<td align="left" width="63%">
Scales the perspective plane of the matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848018(v=VS.85).aspx">SetProduct</a>
</td>
<td align="left" width="63%">
Multiplies the two matrices and stores the result in this matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848019(v=VS.85).aspx">SkewX</a>
</td>
<td align="left" width="63%">
Skews the matrix in the X direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848020(v=VS.85).aspx">SkewY</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Hh848009(v=VS.85).aspx">operator*</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Hh848007(v=VS.85).aspx">Determinant</a>
</td>
<td align="left" width="63%">
Calculates the determinant of the matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848008(v=VS.85).aspx">IsIdentity</a>
</td>
<td align="left" width="63%">
Indicates whether this matrix is the identity matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848010(v=VS.85).aspx">PerspectiveProjection</a>
</td>
<td align="left" width="63%">
A perspective transformation given a depth value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848011(v=VS.85).aspx">ReinterpretBaseType</a>
</td>
<td align="left" width="63%">
Converts the specified <a href="https://msdn.microsoft.com/en-us/library/Dd368132(v=VS.85).aspx">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/204EF85B-BDD4-4A54-96DB-39421F36A75C">ReinterpretBaseType(const D2D1_MATRIX_4X4_F *pMatrix)</a>
</td>
<td align="left" width="63%">
Converts the specified <a href="https://msdn.microsoft.com/en-us/library/Dd368132(v=VS.85).aspx">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848013(v=VS.85).aspx">RotationArbitraryAxis</a>
</td>
<td align="left" width="63%">
Determines the 3-D Rotation matrix for an arbitrary axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848014(v=VS.85).aspx">RotationX</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the X axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848015(v=VS.85).aspx">RotationY</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the Y axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848016(v=VS.85).aspx">RotationZ</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the Z axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848017(v=VS.85).aspx">Scale</a>
</td>
<td align="left" width="63%">
Scales the perspective plane of the matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848018(v=VS.85).aspx">SetProduct</a>
</td>
<td align="left" width="63%">
Multiplies the two matrices and stores the result in this matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848019(v=VS.85).aspx">SkewX</a>
</td>
<td align="left" width="63%">
Skews the matrix in the X direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh848020(v=VS.85).aspx">SkewY</a>
</td>
<td align="left" width="63%">
Skews the matrix in the Y direction.

</td>
</tr>
</table>Calculates the determinant of the matrix.

Indicates whether this matrix is the identity matrix.

A perspective transformation given a depth value.

Converts the specified <a href="https://msdn.microsoft.com/en-us/library/Dd368132(v=VS.85).aspx">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

Converts the specified <a href="https://msdn.microsoft.com/en-us/library/Dd368132(v=VS.85).aspx">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

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
<a href="https://msdn.microsoft.com/en-us/library/Hh848009(v=VS.85).aspx">operator*</a>
</td>
<td align="left" width="63%">
Multiplies this matrix with the specified matrix and returns the result.

</td>
</tr>
</table>Multiplies this matrix with the specified matrix and returns the result.

 

