---
UID: NN:dcomp.IDCompositionVisual
title: IDCompositionVisual (dcomp.h)
author: windows-sdk-content
description: Represents a Microsoft DirectComposition visual.
old-location: directcomp\idcompositionvisual.htm
tech.root: directcomp
ms.assetid: 462dfc20-ad5a-425c-94b5-f21ab05f5af8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual, IDCompositionVisual interface [DirectComposition], IDCompositionVisual interface [DirectComposition],described, dcomp/IDCompositionVisual, directcomp.idcompositionvisual
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
 - IDCompositionVisual
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionVisual interface


## -description


Represents a Microsoft DirectComposition visual. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionVisual</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDCompositionVisual</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionVisual</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-addvisual">AddVisual</a>
</td>
<td align="left" width="63%">
Adds a new child visual to the children list of this visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-removeallvisuals">RemoveAllVisuals</a>
</td>
<td align="left" width="63%">
Removes all visuals from the children list of this visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-removevisual">RemoveVisual</a>
</td>
<td align="left" width="63%">
Removes a child visual from the children list of this visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-setbitmapinterpolationmode">SetBitmapInterpolationMode</a>
</td>
<td align="left" width="63%">
Sets the BitmapInterpolationMode property, which specifies the mode for DirectComposition to use when interpolating pixels from bitmaps that are not axis-aligned or drawn exactly at scale. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-setbordermode">SetBorderMode</a>
</td>
<td align="left" width="63%">
Sets the BorderMode property, which specifies how to compose the edges of bitmaps and clips associated with this visual, or with visuals in the subtree rooted at this visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setclip">SetClip</a>
</td>
<td align="left" width="63%">Overloaded. Sets the Clip property of this visual to the specified rectangular region or clip object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-setcompositemode">SetCompositeMode</a>
</td>
<td align="left" width="63%">
Sets the blending mode for this visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-setcontent">SetContent</a>
</td>
<td align="left" width="63%">
Sets the Content property of this visual to the specified bitmap or window wrapper.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">SetEffect</a>
</td>
<td align="left" width="63%">
Sets the Effect property of this visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449165(v=vs.85)">SetOffsetX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the OffsetX property of this visual, altering the horizontal position of the visual relative to its parent. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449171(v=vs.85)">SetOffsetY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the OffsetY property of this visual, altering the vertical position of the visual relative to its parent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">SetTransform</a>
</td>
<td align="left" width="63%">Overloaded. Sets the Transform property of this visual. The Transform  property specifies a 2D transform used to modify the coordinate system of this visual. The property can specify either a  3-by-2 transform matrix or a transform object.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-settransformparent">SetTransformParent</a>
</td>
<td align="left" width="63%">
Sets the TransformParent property of this visual. The TransformParent property establishes the coordinate system relative to which this visual is composed.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createvisual">IDCompositionDevice::CreateVisual</a>
 

 

