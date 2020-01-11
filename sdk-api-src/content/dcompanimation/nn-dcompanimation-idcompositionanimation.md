---
UID: NN:dcompanimation.IDCompositionAnimation
title: IDCompositionAnimation (dcompanimation.h)
description: Represents a function for animating one or more properties of one or more Microsoft DirectComposition objects.
old-location: directcomp\idcompositionanimation.htm
tech.root: directcomp
ms.assetid: f914e14b-4ac0-4591-9b7f-6b45b88baaaa
ms.date: 12/05/2018
ms.keywords: IDCompositionAnimation, IDCompositionAnimation interface [DirectComposition], IDCompositionAnimation interface [DirectComposition],described, dcompanimation/IDCompositionAnimation, directcomp.idcompositionanimation
f1_keywords:
- dcompanimation/IDCompositionAnimation
dev_langs:
- c++
req.header: dcompanimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DcompAnimation.idl
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
- IDCompositionAnimation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionAnimation interface


## -description


Represents a function for animating one or more  properties of one or more  Microsoft DirectComposition objects. Any object property that takes a scalar value can be animated.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionAnimation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDCompositionAnimation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionAnimation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcompanimation/nf-dcompanimation-idcompositionanimation-addcubic">AddCubic</a>
</td>
<td align="left" width="63%">
Adds a cubic polynomial segment to the animation function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcompanimation/nf-dcompanimation-idcompositionanimation-addrepeat">AddRepeat</a>
</td>
<td align="left" width="63%">
Adds a repeat segment that causes the specified portion of an animation function to be repeated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcompanimation/nf-dcompanimation-idcompositionanimation-addsinusoidal">AddSinusoidal</a>
</td>
<td align="left" width="63%">
Adds a sinusoidal segment to the animation function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcompanimation/nf-dcompanimation-idcompositionanimation-end">End</a>
</td>
<td align="left" width="63%">
Adds an end segment that marks the end of an animation function.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcompanimation/nf-dcompanimation-idcompositionanimation-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the animation function so that it contains no segments.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcompanimation/nf-dcompanimation-idcompositionanimation-setabsolutebegintime">SetAbsoluteBeginTime</a>
</td>
<td align="left" width="63%">
Sets the absolute time at which the animation function starts.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createanimation">IDCompositionDevice::CreateAnimation</a>
 

 

