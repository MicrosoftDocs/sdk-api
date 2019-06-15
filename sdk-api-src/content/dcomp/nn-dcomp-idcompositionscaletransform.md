---
UID: NN:dcomp.IDCompositionScaleTransform
title: IDCompositionScaleTransform (dcomp.h)
author: windows-sdk-content
description: Represents a 2D transformation that affects the scale of a visual along the x-axis and y-axis. The coordinate system is scaled from the specified center point.
old-location: directcomp\idcompositionscaletransform.htm
tech.root: directcomp
ms.assetid: 8e59c484-b7c5-446a-a5d6-e00371e2c08a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionScaleTransform, IDCompositionScaleTransform interface [DirectComposition], IDCompositionScaleTransform interface [DirectComposition],described, dcomp/IDCompositionScaleTransform, directcomp.idcompositionscaletransform
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
 - IDCompositionScaleTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionScaleTransform interface


## -description


Represents a 2D transformation that affects the scale of a visual along the x-axis and y-axis. The coordinate system is scaled from the specified center point. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionScaleTransform</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a>. <b>IDCompositionScaleTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionScaleTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449036(v=vs.85)">SetCenterX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the CenterX property of a 2D scale transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449042(v=vs.85)">SetCenterY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the CenterY property of a 2D scale transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449048(v=vs.85)">SetScaleX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the ScaleX property of a 2D scale transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449055(v=vs.85)">SetScaleY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the ScaleY property of a 2D scale transform.

</td>
</tr>
</table> 


## -remarks



A scale transform represents the following 3-by-3 matrix:

<img alt="Three-by-three scale matrix" src="./images/scale_transform_3x3matrix.png"/>

The effect is to scale the coordinate system up or down and apply the corresponding translation such that the center point does not move.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>
 

 

