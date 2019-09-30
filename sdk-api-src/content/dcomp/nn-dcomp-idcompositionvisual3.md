---
UID: NN:dcomp.IDCompositionVisual3
title: IDCompositionVisual3 (dcomp.h)
author: windows-sdk-content
description: Represents one DirectComposition visual in a visual tree.
old-location: directcomp\idcompositionvisual3.htm
tech.root: directcomp
ms.assetid: c7bf4e6f-119b-2122-1103-d6ab240121c9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual3, IDCompositionVisual3 interface [DirectComposition], IDCompositionVisual3 interface [DirectComposition],described, dcomp/IDCompositionVisual3, directcomp.idcompositionvisual3
ms.topic: interface
f1_keywords: 
 - "dcomp/IDCompositionVisual3"
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDCompositionVisual3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionVisual3 interface


## -description


Represents one DirectComposition visual in a visual tree.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionVisual3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual2">IDCompositionVisual2</a>. <b>IDCompositionVisual3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionVisual3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual3-setdepthmode">SetDepthMode</a>
</td>
<td align="left" width="63%">
Sets the depth mode property associated with this visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/mt589907(v=vs.85)">SetOffsetZ</a>
</td>
<td align="left" width="63%">Overloaded. Sets the value of the visual's OffsetZ property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/directcomp/idcompositionvisual3-setopacity-overloaded">SetOpacity</a>
</td>
<td align="left" width="63%">Overloaded. Sets the value of the visual's opacity property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-settransform">SetTransform</a>
</td>
<td align="left" width="63%">Overloaded. Sets the Transform property of this visual. The Transform  property specifies a 3D transform used to modify the coordinate system of this visual.
  The property can specify either a  4-by-4 transform matrix or a transform object.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn904491(v=vs.85)">SetTransformMode</a>
</td>
<td align="left" width="63%">
Specifies the transform style to be applied to a visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual3-setvisible">SetVisible</a>
</td>
<td align="left" width="63%">
Changes the value of the visual's Visible property.

</td>
</tr>
</table> 


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=313910">DirectComposition Backface and D2D Batching</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual2">IDCompositionVisual2</a>



<b>Sample</b>
 

 

