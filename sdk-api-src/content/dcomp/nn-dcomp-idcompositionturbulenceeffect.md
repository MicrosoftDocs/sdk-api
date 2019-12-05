---
UID: NN:dcomp.IDCompositionTurbulenceEffect
title: IDCompositionTurbulenceEffect (dcomp.h)
description: The turbulence effect is used to generate a bitmap based on the Perlin noise function. The turbulence effect has no input image.
old-location: directcomp\idcompositionturbulenceeffect.htm
tech.root: directcomp
ms.assetid: 6A0100DE-DB63-475C-BF7D-3B2D436704A5
ms.date: 12/05/2018
ms.keywords: IDCompositionTurbulenceEffect, IDCompositionTurbulenceEffect interface [DirectComposition], IDCompositionTurbulenceEffect interface [DirectComposition],described, dcomp/IDCompositionTurbulenceEffect, directcomp.idcompositionturbulenceeffect
ms.topic: interface
f1_keywords:
- dcomp/IDCompositionTurbulenceEffect
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
- IDCompositionTurbulenceEffect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionTurbulenceEffect interface


## -description


The turbulence effect is used to generate a bitmap based on the Perlin noise function.
          The turbulence effect has no input image.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionTurbulenceEffect</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionfiltereffect">IDCompositionFilterEffect</a>. <b>IDCompositionTurbulenceEffect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionTurbulenceEffect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionturbulenceeffect-setbasefrequency">SetBaseFrequency</a>
</td>
<td align="left" width="63%">
Sets the base frequencies in the X and Y direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionturbulenceeffect-setnoise">SetNoise</a>
</td>
<td align="left" width="63%">
Sets the turbulence noise mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionturbulenceeffect-setnumoctaves">SetNumOctaves</a>
</td>
<td align="left" width="63%">
Sets the number of octaves for the noise function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionturbulenceeffect-setoffset">SetOffset</a>
</td>
<td align="left" width="63%">
Sets the coordinates where the turbulence output is generated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionturbulenceeffect-setseed">SetSeed</a>
</td>
<td align="left" width="63%">
Sets the seed for the pseudo random generator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionturbulenceeffect-setsize">SetSize</a>
</td>
<td align="left" width="63%">
Sets the size of the turbulence output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionturbulenceeffect-setstitchable">SetStitchable</a>
</td>
<td align="left" width="63%">
Specifies whether stitching is on or off.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionfiltereffect">IDCompositionFilterEffect</a>
 

 

