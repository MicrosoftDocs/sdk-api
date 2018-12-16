---
UID: NN:dcomp.IDCompositionTurbulenceEffect
title: IDCompositionTurbulenceEffect
author: windows-sdk-content
description: The turbulence effect is used to generate a bitmap based on the Perlin noise function. The turbulence effect has no input image.
old-location: directcomp\idcompositionturbulenceeffect.htm
tech.root: directcomp
ms.assetid: 6A0100DE-DB63-475C-BF7D-3B2D436704A5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionTurbulenceEffect, IDCompositionTurbulenceEffect interface [DirectComposition], IDCompositionTurbulenceEffect interface [DirectComposition],described, dcomp/IDCompositionTurbulenceEffect, directcomp.idcompositionturbulenceeffect
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionTurbulenceEffect interface


## -description


The turbulence effect is used to generate a bitmap based on the Perlin noise function.
          The turbulence effect has no input image.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionTurbulenceEffect</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dn919730(v=VS.85).aspx">IDCompositionFilterEffect</a>. <b>IDCompositionTurbulenceEffect</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dn919802(v=VS.85).aspx">SetBaseFrequency</a>
</td>
<td align="left" width="63%">
Sets the base frequencies in the X and Y direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn919803(v=VS.85).aspx">SetNoise</a>
</td>
<td align="left" width="63%">
Sets the turbulence noise mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn919804(v=VS.85).aspx">SetNumOctaves</a>
</td>
<td align="left" width="63%">
Sets the number of octaves for the noise function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn919805(v=VS.85).aspx">SetOffset</a>
</td>
<td align="left" width="63%">
Sets the coordinates where the turbulence output is generated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn919806(v=VS.85).aspx">SetSeed</a>
</td>
<td align="left" width="63%">
Sets the seed for the pseudo random generator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn919807(v=VS.85).aspx">SetSize</a>
</td>
<td align="left" width="63%">
Sets the size of the turbulence output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn919808(v=VS.85).aspx">SetStitchable</a>
</td>
<td align="left" width="63%">
Specifies whether stitching is on or off.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn919730(v=VS.85).aspx">IDCompositionFilterEffect</a>
 

 

