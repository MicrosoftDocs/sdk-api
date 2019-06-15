---
UID: NN:dcomp.IDCompositionRotateTransform3D
title: IDCompositionRotateTransform3D (dcomp.h)
author: windows-sdk-content
description: Represents a 3D transformation that affects the rotation of a visual along an arbitrary axis in 3D space. The coordinate system is rotated around the specified center point.
old-location: directcomp\idcompositionrotatetransform3d.htm
tech.root: directcomp
ms.assetid: BEC58B57-66A1-4645-A0B8-D546334E1E23
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform3D, IDCompositionRotateTransform3D interface [DirectComposition], IDCompositionRotateTransform3D interface [DirectComposition],described, dcomp/IDCompositionRotateTransform3D, directcomp.idcompositionrotatetransform3d
ms.topic: interface
f1_keywords: ["dcomp/IDCompositionRotateTransform3D"]
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionRotateTransform3D
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionRotateTransform3D interface


## -description


Represents a 3D transformation that affects the rotation of a visual along an arbitrary axis in 3D space. The coordinate system is rotated around the specified center point. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionRotateTransform3D</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform3d">IDCompositionTransform3D</a>. <b>IDCompositionRotateTransform3D</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionRotateTransform3D</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh448933(v=vs.85)">SetAngle</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the Angle property of a 3D rotation transform. The Angle property specifies the rotation angle, in degrees. The default value is zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setaxisx">SetAxisX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the AxisX property of a 3D rotation transform. The AxisX property specifies the x-coordinate for the axis vector of rotation. The default value is zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setaxisy">SetAxisY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the AxisY property of a rotation transform. The AxisY property specifies the y-coordinate for the axis vector of rotation.  The default value is zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setaxisz">SetAxisZ</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the AxisZ property of a 3D rotation transform. The AxisZ property specifies the z-coordinate for the axis vector of rotation. The default value is 1.0.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setcenterx">SetCenterX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the CenterX property of a 3D rotation transform. The CenterX property specifies the x-coordinate of the point about which the rotation is performed. The default value is zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setcentery">SetCenterY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the CenterY property of a 3D rotation transform. The CenterY property specifies the y-coordinate of the point about which the rotation is performed. The default value is zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setcenterz">SetCenterZ</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the CenterZ property of a 3D rotation transform. The CenterZ property specifies the z-coordinate of the point about which the rotation is performed. The default value is zero.

</td>
</tr>
</table> 


## -remarks



A 3D rotate transform represents the following 4-by-4 matrix:

<img alt="Four-by-four 3D rotate transformation matrix" src="./images/3D_rotate_transform_4x4matrix.png"/>

where the <i>offsetX</i>, <i>offsetY</i>, and <i>offsetZ</i> values of the matrix are the following: 

<img alt="Values of the four-by-four 3D rotate transformation matrix" src="./images/3D_rotate_transform_matrix_values.png"/>

The effect is to rotate the coordinate system clockwise or counter-clockwise around the specified axis, and to apply the corresponding translation such that the center point does not move.

A new 3D rotation transform object has a default static value of zero for the Angle, CenterX, CenterY, AxisX, and AxisY properties, and a default static value of 1.0 for the AxisZ property.

When setting the axis to a non-default value, you should always set all three axis properties (AxisX, AxisY, and AxisZ).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositioneffectgroup-settransform3d">IDCompositionEffectGroup::SetTransform3D</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform3d">IDCompositionTransform3D</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">IDCompositionVisual::SetEffect</a>
 

 

