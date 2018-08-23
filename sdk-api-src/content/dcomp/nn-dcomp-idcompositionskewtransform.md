---
UID: NN:dcomp.IDCompositionSkewTransform
title: IDCompositionSkewTransform
author: windows-sdk-content
description: Represents a 2D transformation that affects the skew of a visual along the x-axis and y-axis. The coordinate system is skewed around the specified center point.
old-location: directcomp\idcompositionskewtransform.htm
old-project: directcomp
ms.assetid: c1dbc11f-b8e3-487e-84f0-517ebaf65de8
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDCompositionSkewTransform, IDCompositionSkewTransform interface [DirectComposition], IDCompositionSkewTransform interface [DirectComposition],described, dcomp/IDCompositionSkewTransform, directcomp.idcompositionskewtransform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dcomp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D_VECTOR_4F
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionSkewTransform
product: Windows
targetos: Windows
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
---

# IDCompositionSkewTransform interface


## -description


Represents a 2D transformation that affects the skew of a visual along the x-axis and y-axis. The coordinate system is skewed around the specified center point. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionSkewTransform</b> interface inherits from <a href="https://msdn.microsoft.com/22f0d199-5162-4869-909e-d0ed0059b773">IDCompositionTransform</a>. <b>IDCompositionSkewTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionSkewTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DA4AEE0D-A913-434E-9150-DD6763132041">SetAngleX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the AngleX property of a 2D skew transform. The AngleX property specifies the rotation angle, in degrees. The default value is zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BD3D282C-5BBD-4BCE-AE15-4491A37D9149">SetAngleY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the AngleY property of a 2D skew transform. The AngleY property specifies the rotation angle, in degrees. The default value is zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/934E3D60-45F4-4645-8E77-22F7E4AEAD60">SetCenterX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the CenterX property of a 2D skew transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D3F5E009-D6D2-431F-AC5C-C14C0AE1CD36">SetCenterY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the CenterY property of a  of a 2D skew transform.

</td>
</tr>
</table> 


## -remarks



A skew transform represents the following 3-by-3 matrix: 

<img alt="Three-by-three skew matrix" src="images/skew_transform_3x3matrix.png"/>

The effect is to slant the coordinate system along the x-axis and y-axis such that a rectangle becomes a parallelogram, and to apply the corresponding translation such that the center point does not move.




## -see-also




<a href="https://msdn.microsoft.com/22f0d199-5162-4869-909e-d0ed0059b773">IDCompositionTransform</a>



<a href="https://msdn.microsoft.com/DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D">IDCompositionVisual::SetTransform</a>
 

 

