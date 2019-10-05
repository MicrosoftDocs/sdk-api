---
UID: NN:dcomp.IDCompositionArithmeticCompositeEffect
title: IDCompositionArithmeticCompositeEffect (dcomp.h)
author: windows-sdk-content
description: The arithmetic composite effect is used to combine 2 images using a weighted sum of pixels from the input images.
old-location: directcomp\idcompositionarithmeticcompositeeffect.htm
tech.root: directcomp
ms.assetid: 06430DD6-B6BF-4F55-A99C-13860B800444
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionArithmeticCompositeEffect, IDCompositionArithmeticCompositeEffect interface [DirectComposition], IDCompositionArithmeticCompositeEffect interface [DirectComposition],described, dcomp/IDCompositionArithmeticCompositeEffect, directcomp.idcompositionarithmeticcompositeeffect
ms.topic: interface
f1_keywords: 
 - "dcomp/IDCompositionArithmeticCompositeEffect"
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
 - IDCompositionArithmeticCompositeEffect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionArithmeticCompositeEffect interface


## -description


The arithmetic composite effect is used to combine 2 images using a weighted sum of pixels from the input images.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionArithmeticCompositeEffect</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionfiltereffect">IDCompositionFilterEffect</a>. <b>IDCompositionArithmeticCompositeEffect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionArithmeticCompositeEffect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionarithmeticcompositeeffect-setclampoutput">SetClampOutput</a>
</td>
<td align="left" width="63%">
Specifies whether to clamp color values before the effect passes the values to the next effect in the graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setcoefficient1">SetCoefficient1</a>
</td>
<td align="left" width="63%">Overloaded. Sets the first coefficient for the equation used to composite the two input images.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setcoefficient2">setcoefficient2</a>
</td>
<td align="left" width="63%">Overloaded. Sets the second coefficient for the equation used to composite the two input images.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setcoefficient3">setcoefficient3</a>
</td>
<td align="left" width="63%">Overloaded. Sets the third coefficient for the equation used to composite the two input images.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setcoefficient4">SetCoefficient4</a>
</td>
<td align="left" width="63%">Overloaded. Sets the fourth coefficient for the equation used to composite the two input images.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionarithmeticcompositeeffect-setcoefficients">SetCoefficients</a>
</td>
<td align="left" width="63%">
Sets the coefficients for the equation used to composite the two input images.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionfiltereffect">IDCompositionFilterEffect</a>
 

 

