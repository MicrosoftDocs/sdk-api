---
UID: NN:dcomp.IDCompositionRotateTransform3D
title: IDCompositionRotateTransform3D
author: windows-sdk-content
description: Represents a 3D transformation that affects the rotation of a visual along an arbitrary axis in 3D space. The coordinate system is rotated around the specified center point.
old-location: directcomp\idcompositionrotatetransform3d.htm
tech.root: directcomp
ms.assetid: BEC58B57-66A1-4645-A0B8-D546334E1E23
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IDCompositionRotateTransform3D, IDCompositionRotateTransform3D interface [DirectComposition], IDCompositionRotateTransform3D interface [DirectComposition],described, dcomp/IDCompositionRotateTransform3D, directcomp.idcompositionrotatetransform3d
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# IDCompositionRotateTransform3D interface


## -description


Represents a 3D transformation that affects the rotation of a visual along an arbitrary axis in 3D space. The coordinate system is rotated around the specified center point. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionRotateTransform3D</b> interface inherits from <a href="https://msdn.microsoft.com/81239AB4-C2A3-4E37-95E3-B3C10532EE15">IDCompositionTransform3D</a>. <b>IDCompositionRotateTransform3D</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/12BEE73C-195A-42B5-A1BC-B5235440AC43">SetAngle</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the Angle property of a 3D rotation transform. The Angle property specifies the rotation angle, in degrees. The default value is zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ADBB027-8F80-4DF3-9199-DDB6570DF81B">SetAxisX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the AxisX property of a 3D rotation transform. The AxisX property specifies the x-coordinate for the axis vector of rotation. The default value is zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C86E4D59-4E9D-44BF-BA9D-91714D0C2D37">SetAxisY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the AxisY property of a rotation transform. The AxisY property specifies the y-coordinate for the axis vector of rotation.  The default value is zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1A96FA00-20FE-4876-B7DF-2B833B17E925">SetAxisZ</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the AxisZ property of a 3D rotation transform. The AxisZ property specifies the z-coordinate for the axis vector of rotation. The default value is 1.0.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2E4924A5-64D0-4415-B345-0DE9A0900258">SetCenterX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the CenterX property of a 3D rotation transform. The CenterX property specifies the x-coordinate of the point about which the rotation is performed. The default value is zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19B3B065-BE8C-4CBD-8A94-54934CA0B421">SetCenterY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the CenterY property of a 3D rotation transform. The CenterY property specifies the y-coordinate of the point about which the rotation is performed. The default value is zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7FF293B6-8FAE-4277-8C07-EBD4E819E2A0">SetCenterZ</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the CenterZ property of a 3D rotation transform. The CenterZ property specifies the z-coordinate of the point about which the rotation is performed. The default value is zero.

</td>
</tr>
</table> 


## -remarks



A 3D rotate transform represents the following 4-by-4 matrix:

<img alt="Four-by-four 3D rotate transformation matrix" src="images/3D_rotate_transform_4x4matrix.png"/>

where the <i>offsetX</i>, <i>offsetY</i>, and <i>offsetZ</i> values of the matrix are the following: 

<img alt="Values of the four-by-four 3D rotate transformation matrix" src="images/3D_rotate_transform_matrix_values.png"/>

The effect is to rotate the coordinate system clockwise or counter-clockwise around the specified axis, and to apply the corresponding translation such that the center point does not move.

A new 3D rotation transform object has a default static value of zero for the Angle, CenterX, CenterY, AxisX, and AxisY properties, and a default static value of 1.0 for the AxisZ property.

When setting the axis to a non-default value, you should always set all three axis properties (AxisX, AxisY, and AxisZ).




## -see-also




<a href="https://msdn.microsoft.com/40935581-D45C-496B-90B9-152963F0B55A">IDCompositionEffectGroup::SetTransform3D</a>



<a href="https://msdn.microsoft.com/81239AB4-C2A3-4E37-95E3-B3C10532EE15">IDCompositionTransform3D</a>



<a href="https://msdn.microsoft.com/CCA785F6-869C-460A-AF54-573BDE798685">IDCompositionVisual::SetEffect</a>
 

 

