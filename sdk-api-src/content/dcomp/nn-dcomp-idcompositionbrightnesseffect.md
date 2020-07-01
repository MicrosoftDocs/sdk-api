---
UID: NN:dcomp.IDCompositionBrightnessEffect
title: IDCompositionBrightnessEffect (dcomp.h)
description: The brightness effect controls the brightness of the image.
helpviewer_keywords: ["IDCompositionBrightnessEffect","IDCompositionBrightnessEffect interface [DirectComposition]","IDCompositionBrightnessEffect interface [DirectComposition]","described","dcomp/IDCompositionBrightnessEffect","directcomp.idcompositionbrightnesseffect"]
old-location: directcomp\idcompositionbrightnesseffect.htm
tech.root: directcomp
ms.assetid: 22503D7B-A359-4877-A437-6A97D8835BC7
ms.date: 12/05/2018
ms.keywords: IDCompositionBrightnessEffect, IDCompositionBrightnessEffect interface [DirectComposition], IDCompositionBrightnessEffect interface [DirectComposition],described, dcomp/IDCompositionBrightnessEffect, directcomp.idcompositionbrightnesseffect
f1_keywords:
- dcomp/IDCompositionBrightnessEffect
dev_langs:
- c++
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
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
- IDCompositionBrightnessEffect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionBrightnessEffect interface


## -description


The brightness effect controls the brightness of the image.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionBrightnessEffect</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionfiltereffect">IDCompositionFilterEffect</a>. <b>IDCompositionBrightnessEffect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionBrightnessEffect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionbrightnesseffect-setblackpoint">SetBlackPoint</a>
</td>
<td align="left" width="63%">
Specifies the lower portion of the brightness transfer curve for the brightness effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setblackpointx">SetBlackPointX</a>
</td>
<td align="left" width="63%">Overloaded. Sets the x value of the black point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setblackpointy">SetBlackPointY</a>
</td>
<td align="left" width="63%">Overloaded. Sets the y value of the black point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionbrightnesseffect-setwhitepoint">SetWhitePoint</a>
</td>
<td align="left" width="63%">
Sets the upper portion of the brightness transfer curve. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setwhitepointx">SetWhitePointX</a>
</td>
<td align="left" width="63%">Overloaded. Sets the x value of the white point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setwhitepointy">SetWhitePointY</a>
</td>
<td align="left" width="63%">Overloaded. Sets the y value of the white point.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionfiltereffect">IDCompositionFilterEffect</a>
 

 

