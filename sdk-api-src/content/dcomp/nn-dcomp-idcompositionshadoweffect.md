---
UID: NN:dcomp.IDCompositionShadowEffect
title: IDCompositionShadowEffect
author: windows-sdk-content
description: The shadow effect is used to generate a shadow from the alpha channel of an image. The shadow is more opaque for higher alpha values and more transparent for lower alpha values. You can set the amount of blur and the color of the shadow.
old-location: directcomp\idcompositionshadoweffect.htm
tech.root: directcomp
ms.assetid: 115FD667-64D2-4538-9EB4-B133D5DCAF30
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDCompositionShadowEffect, IDCompositionShadowEffect interface [DirectComposition], IDCompositionShadowEffect interface [DirectComposition],described, dcomp/IDCompositionShadowEffect, directcomp.idcompositionshadoweffect
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
 - IDCompositionShadowEffect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionShadowEffect interface


## -description


The shadow effect is used to generate a shadow from the alpha channel of an image. The shadow is more opaque for higher alpha values and more transparent for lower alpha values.
          You can set the amount of blur and the color of the shadow.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionShadowEffect</b> interface inherits from <a href="https://msdn.microsoft.com/4303c24d-e3e1-e188-bbef-e654c0e7e266">IDCompositionFilterEffect</a>. <b>IDCompositionShadowEffect</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c65a6f89-9135-c673-ff05-ad26329da2cb">SetAlpha</a>
</td>
<td align="left" width="63%">Overloaded. Sets the alpha value for the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ef324ce-8a62-ebca-45ca-3c92671dfaa3">SetBlue</a>
</td>
<td align="left" width="63%">Overloaded. Sets the blue value for the color of the shadow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1C08E464-087A-41BF-9B0E-E1370576E64A">SetColor</a>
</td>
<td align="left" width="63%">
Sets color of the shadow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1a74aca-6026-1307-7300-ca2941246000">SetRed</a>
</td>
<td align="left" width="63%">Overloaded. Sets the red value for the color of the shadow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c688967e-9daf-63f7-9275-aa7b4b871246">SetStandardDeviation</a>
</td>
<td align="left" width="63%">Overloaded. Sets the amount of blur to be applied to the alpha channel of the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55566eb3-939e-c61f-dae8-5bd8da1c9f5b">V</a>
</td>
<td align="left" width="63%">Overloaded. Sets the green value for the color of the shadow.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4303c24d-e3e1-e188-bbef-e654c0e7e266">IDCompositionFilterEffect</a>
 

 

