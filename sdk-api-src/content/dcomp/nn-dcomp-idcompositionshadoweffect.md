---
UID: NN:dcomp.IDCompositionShadowEffect
title: IDCompositionShadowEffect (dcomp.h)
author: windows-sdk-content
description: The shadow effect is used to generate a shadow from the alpha channel of an image. The shadow is more opaque for higher alpha values and more transparent for lower alpha values. You can set the amount of blur and the color of the shadow.
old-location: directcomp\idcompositionshadoweffect.htm
tech.root: directcomp
ms.assetid: 115FD667-64D2-4538-9EB4-B133D5DCAF30
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionShadowEffect, IDCompositionShadowEffect interface [DirectComposition], IDCompositionShadowEffect interface [DirectComposition],described, dcomp/IDCompositionShadowEffect, directcomp.idcompositionshadoweffect
ms.topic: interface
f1_keywords: 
 - "dcomp/IDCompositionShadowEffect"
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
 - IDCompositionShadowEffect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionShadowEffect interface


## -description


The shadow effect is used to generate a shadow from the alpha channel of an image. The shadow is more opaque for higher alpha values and more transparent for lower alpha values.
          You can set the amount of blur and the color of the shadow.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionShadowEffect</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionfiltereffect">IDCompositionFilterEffect</a>. <b>IDCompositionShadowEffect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionShadowEffect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/directcomp/idcompositionshadoweffect-setalpha-overloaded">SetAlpha</a>
</td>
<td align="left" width="63%">Overloaded. Sets the alpha value for the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setblue">SetBlue</a>
</td>
<td align="left" width="63%">Overloaded. Sets the blue value for the color of the shadow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionshadoweffect-setcolor">SetColor</a>
</td>
<td align="left" width="63%">
Sets color of the shadow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setred">SetRed</a>
</td>
<td align="left" width="63%">Overloaded. Sets the red value for the color of the shadow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn905304(v=vs.85)">SetStandardDeviation</a>
</td>
<td align="left" width="63%">Overloaded. Sets the amount of blur to be applied to the alpha channel of the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn905302(v=vs.85)">V</a>
</td>
<td align="left" width="63%">Overloaded. Sets the green value for the color of the shadow.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionfiltereffect">IDCompositionFilterEffect</a>
 

 

