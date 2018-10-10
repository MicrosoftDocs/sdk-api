---
UID: NN:dcomp.IDCompositionScaleTransform3D
title: IDCompositionScaleTransform3D
author: windows-sdk-content
description: Represents a 3D transformation effect that affects the scale of a visual along the x-axis, y-axis, and z-axis. The coordinate system is scaled from the specified center point.
old-location: directcomp\idcompositionscaletransform3d.htm
tech.root: directcomp
ms.assetid: 0526B772-EA84-40B2-88D6-CFB1A70A1D5A
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IDCompositionScaleTransform3D, IDCompositionScaleTransform3D interface [DirectComposition], IDCompositionScaleTransform3D interface [DirectComposition],described, dcomp/IDCompositionScaleTransform3D, directcomp.idcompositionscaletransform3d
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
 - IDCompositionScaleTransform3D
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionScaleTransform3D interface


## -description


Represents a 3D transformation effect that affects the scale of a visual along the x-axis, y-axis, and z-axis. The coordinate system is scaled from the specified center point. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionScaleTransform3D</b> interface inherits from <a href="https://msdn.microsoft.com/81239AB4-C2A3-4E37-95E3-B3C10532EE15">IDCompositionTransform3D</a>. <b>IDCompositionScaleTransform3D</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionScaleTransform3D</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/959F8530-D2D5-46BC-9F29-F1DFC8029C12">SetCenterX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the CenterX property of a 3D scale transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C650032E-3344-4BE8-9018-F57EFECEBF61">SetCenterY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the CenterY property of a 3D scale transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1A5C63FE-2378-4274-8ADD-04A88B60FF8F">SetCenterZ</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the CenterZ property of a 3D scale transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96A7B9EC-7CD9-489F-AB97-A297321BDACD">SetScaleX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the ScaleX property of a 3D scale transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90E48F55-B9A3-464D-9FB2-03AA27AA5A08">SetScaleY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the ScaleY property of a scale transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CD00FBB3-246E-45D0-A7F6-5A7F9C37376B">SetScaleZ</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the ScaleZ property of a scale transform.

</td>
</tr>
</table> 


## -remarks



A 3D scale transform represents the following 4-by-4 matrix:

<img alt="Four-by-four 3D scale matrix" src="images/3D_scale_transform_4x4matrix.png"/>

The effect is to scale the blending of the visual's subtree up or down, and apply the corresponding translation such that the center point does not move.




## -see-also




<a href="https://msdn.microsoft.com/40935581-D45C-496B-90B9-152963F0B55A">IDCompositionEffectGroup::SetTransform3D</a>



<a href="https://msdn.microsoft.com/81239AB4-C2A3-4E37-95E3-B3C10532EE15">IDCompositionTransform3D</a>



<a href="https://msdn.microsoft.com/CCA785F6-869C-460A-AF54-573BDE798685">IDCompositionVisual::SetEffect</a>
 

 

