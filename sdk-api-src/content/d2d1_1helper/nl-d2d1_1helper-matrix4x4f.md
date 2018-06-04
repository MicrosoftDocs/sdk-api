---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# Matrix4x4F class


## -description


The <b>Matrix4x4F</b> class represents a 4-by-4 matrix and provides convenience methods for creating matrices.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">Matrix4x4F</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Operators</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>Matrix4x4F</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/900531EB-F3D4-4971-984E-A355E79D6577">Determinant</a>
</td>
<td align="left" width="63%">
Calculates the determinant of the matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60793CCB-F3E9-4647-9DB0-E28FF1AD0E22">IsIdentity</a>
</td>
<td align="left" width="63%">
Indicates whether this matrix is the identity matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AE896E2E-752E-46D1-9281-4B3511D21468">PerspectiveProjection</a>
</td>
<td align="left" width="63%">
A perspective transformation given a depth value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/379F9F01-EE5E-438B-BD0A-F0EB6B92E28F">ReinterpretBaseType</a>
</td>
<td align="left" width="63%">
Converts the specified <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/204EF85B-BDD4-4A54-96DB-39421F36A75C">ReinterpretBaseType(const D2D1_MATRIX_4X4_F *pMatrix)</a>
</td>
<td align="left" width="63%">
Converts the specified <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/396C3F62-0662-4518-AD1E-8B53B96D1CDD">RotationArbitraryAxis</a>
</td>
<td align="left" width="63%">
Determines the 3-D Rotation matrix for an arbitrary axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3F9B9CE2-18F4-4F73-9725-A10B84639817">RotationX</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the X axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F761CAB1-77F8-4C98-9085-3FBF4452AA51">RotationY</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the Y axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4E17EE04-C4B9-49AC-819A-9518937B78F9">RotationZ</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the Z axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D0ACA5DC-D144-4832-94EB-A851F7602FD9">Scale</a>
</td>
<td align="left" width="63%">
Scales the perspective plane of the matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CC12D975-B08A-4671-9F61-CBAC343AC126">SetProduct</a>
</td>
<td align="left" width="63%">
Multiplies the two matrices and stores the result in this matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6102EAEA-24B5-43C2-9351-3E9F3D06F6D3">SkewX</a>
</td>
<td align="left" width="63%">
Skews the matrix in the X direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/481D428F-C070-4112-83BB-3B4E8E0C7319">SkewY</a>
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
<a href="https://msdn.microsoft.com/2ED3EF0A-84B9-4BE9-825B-EA55DE2BAF47">operator*</a>
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
<a href="https://msdn.microsoft.com/900531EB-F3D4-4971-984E-A355E79D6577">Determinant</a>
</td>
<td align="left" width="63%">
Calculates the determinant of the matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60793CCB-F3E9-4647-9DB0-E28FF1AD0E22">IsIdentity</a>
</td>
<td align="left" width="63%">
Indicates whether this matrix is the identity matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AE896E2E-752E-46D1-9281-4B3511D21468">PerspectiveProjection</a>
</td>
<td align="left" width="63%">
A perspective transformation given a depth value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/379F9F01-EE5E-438B-BD0A-F0EB6B92E28F">ReinterpretBaseType</a>
</td>
<td align="left" width="63%">
Converts the specified <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/204EF85B-BDD4-4A54-96DB-39421F36A75C">ReinterpretBaseType(const D2D1_MATRIX_4X4_F *pMatrix)</a>
</td>
<td align="left" width="63%">
Converts the specified <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/396C3F62-0662-4518-AD1E-8B53B96D1CDD">RotationArbitraryAxis</a>
</td>
<td align="left" width="63%">
Determines the 3-D Rotation matrix for an arbitrary axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3F9B9CE2-18F4-4F73-9725-A10B84639817">RotationX</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the X axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F761CAB1-77F8-4C98-9085-3FBF4452AA51">RotationY</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the Y axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4E17EE04-C4B9-49AC-819A-9518937B78F9">RotationZ</a>
</td>
<td align="left" width="63%">
Rotates the transform matrix around the Z axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D0ACA5DC-D144-4832-94EB-A851F7602FD9">Scale</a>
</td>
<td align="left" width="63%">
Scales the perspective plane of the matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CC12D975-B08A-4671-9F61-CBAC343AC126">SetProduct</a>
</td>
<td align="left" width="63%">
Multiplies the two matrices and stores the result in this matrix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6102EAEA-24B5-43C2-9351-3E9F3D06F6D3">SkewX</a>
</td>
<td align="left" width="63%">
Skews the matrix in the X direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/481D428F-C070-4112-83BB-3B4E8E0C7319">SkewY</a>
</td>
<td align="left" width="63%">
Skews the matrix in the Y direction.

</td>
</tr>
</table>Calculates the determinant of the matrix.

Indicates whether this matrix is the identity matrix.

A perspective transformation given a depth value.

Converts the specified <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

Converts the specified <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_4X4_F</a> matrix to a <b>Matrix4x4F</b> without making a copy.

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
<a href="https://msdn.microsoft.com/2ED3EF0A-84B9-4BE9-825B-EA55DE2BAF47">operator*</a>
</td>
<td align="left" width="63%">
Multiplies this matrix with the specified matrix and returns the result.

</td>
</tr>
</table>Multiplies this matrix with the specified matrix and returns the result.

 

