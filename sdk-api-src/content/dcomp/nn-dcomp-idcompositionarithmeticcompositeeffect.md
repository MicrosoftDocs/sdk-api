---
UID: NN:dcomp.IDCompositionArithmeticCompositeEffect
title: IDCompositionArithmeticCompositeEffect
author: windows-sdk-content
description: The arithmetic composite effect is used to combine 2 images using a weighted sum of pixels from the input images.
old-location: directcomp\idcompositionarithmeticcompositeeffect.htm
tech.root: directcomp
ms.assetid: 06430DD6-B6BF-4F55-A99C-13860B800444
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IDCompositionArithmeticCompositeEffect, IDCompositionArithmeticCompositeEffect interface [DirectComposition], IDCompositionArithmeticCompositeEffect interface [DirectComposition],described, dcomp/IDCompositionArithmeticCompositeEffect, directcomp.idcompositionarithmeticcompositeeffect
ms.prod: windows
ms.technology: windows-sdk
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
 - IDCompositionArithmeticCompositeEffect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionArithmeticCompositeEffect interface


## -description


The arithmetic composite effect is used to combine 2 images using a weighted sum of pixels from the input images.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionArithmeticCompositeEffect</b> interface inherits from <a href="https://msdn.microsoft.com/4303c24d-e3e1-e188-bbef-e654c0e7e266">IDCompositionFilterEffect</a>. <b>IDCompositionArithmeticCompositeEffect</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6558E6E7-FEF3-43F0-8508-197BA1DE3D10">SetClampOutput</a>
</td>
<td align="left" width="63%">
Specifies whether to clamp color values before the effect passes the values to the next effect in the graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74b18201-5710-1213-51f8-2f97ba86c9a4">SetCoefficient1</a>
</td>
<td align="left" width="63%">Overloaded. Sets the first coefficient for the equation used to composite the two input images.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58ecefbe-ca31-3c13-7bea-e97fb73753e2">setcoefficient2</a>
</td>
<td align="left" width="63%">Overloaded. Sets the second coefficient for the equation used to composite the two input images.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d330b4e-6ddd-2a9a-6a30-e459c9669c85">setcoefficient3</a>
</td>
<td align="left" width="63%">Overloaded. Sets the third coefficient for the equation used to composite the two input images.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adaa5348-3887-d3ba-dad1-e49310815cc2">SetCoefficient4</a>
</td>
<td align="left" width="63%">Overloaded. Sets the fourth coefficient for the equation used to composite the two input images.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02A98C38-1D6E-43ED-8744-D3029F4BF573">SetCoefficients</a>
</td>
<td align="left" width="63%">
Sets the coefficients for the equation used to composite the two input images.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4303c24d-e3e1-e188-bbef-e654c0e7e266">IDCompositionFilterEffect</a>
 

 

