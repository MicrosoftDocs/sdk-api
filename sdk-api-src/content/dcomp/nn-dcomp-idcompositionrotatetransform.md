---
UID: NN:dcomp.IDCompositionRotateTransform
title: IDCompositionRotateTransform (dcomp.h)
author: windows-sdk-content
description: Represents a 2D transformation that affects the rotation of a visual around the z-axis. The coordinate system is rotated around the specified center point.
old-location: directcomp\idcompositionrotatetransform.htm
tech.root: directcomp
ms.assetid: 6c92bd6b-4479-45c2-986c-0a6c91248361
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform, IDCompositionRotateTransform interface [DirectComposition], IDCompositionRotateTransform interface [DirectComposition],described, dcomp/IDCompositionRotateTransform, directcomp.idcompositionrotatetransform
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
 - IDCompositionRotateTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionRotateTransform interface


## -description


Represents a 2D transformation that affects the rotation of a visual around the z-axis. The coordinate system is rotated around the specified center point. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionRotateTransform</b> interface inherits from <a href="https://msdn.microsoft.com/22f0d199-5162-4869-909e-d0ed0059b773">IDCompositionTransform</a>. <b>IDCompositionRotateTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionRotateTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8AE92567-B5A3-47A2-A652-4D777F62019D">SetAngle</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the Angle property of a rotation transform. The Angle property specifies the rotation angle, in degrees. The default value is zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D5CE4491-0A06-4824-BDE5-A839E0E60EA7">SetCenterX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the CenterX property of a 2D rotation transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4C586C46-AA3E-4572-AFD6-8661BD26AC50">SetCenterY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the CenterY property of a 2D rotation transform.

</td>
</tr>
</table> 


## -remarks



A rotate transform represents the following 3-by-3 matrix:

<img alt="Three-by-three transformation matrix" src="./images/rotate_transform_3x3matrix.png"/>

The effect is to rotate the coordinate system clockwise or counter-clockwise, and to apply the corresponding translation such that the center point does not move.




## -see-also




<a href="https://msdn.microsoft.com/22f0d199-5162-4869-909e-d0ed0059b773">IDCompositionTransform</a>



<a href="https://msdn.microsoft.com/DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D">IDCompositionVisual::SetTransform</a>
 

 

