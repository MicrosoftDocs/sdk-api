---
UID: NN:dcomp.IDCompositionLinearTransferEffect
title: IDCompositionLinearTransferEffect (dcomp.h)
author: windows-sdk-content
description: The linear transfer effect is used to map the color intensities of an image using a linear function created from a list of values you provide for each channel.
old-location: directcomp\idcompositionlineartransfereffect.htm
tech.root: directcomp
ms.assetid: 516CD029-DBB1-4AD7-92BB-8B6EF6C733FA
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionLinearTransferEffect, IDCompositionLinearTransferEffect interface [DirectComposition], IDCompositionLinearTransferEffect interface [DirectComposition],described, dcomp/IDCompositionLinearTransferEffect, directcomp.idcompositionlineartransfereffect
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
 - IDCompositionLinearTransferEffect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionLinearTransferEffect interface


## -description


The linear transfer effect is used to map the color intensities of an image using a linear function created from a list of values you provide for each channel.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionLinearTransferEffect</b> interface inherits from <a href="https://msdn.microsoft.com/4303c24d-e3e1-e188-bbef-e654c0e7e266">IDCompositionFilterEffect</a>. <b>IDCompositionLinearTransferEffect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionLinearTransferEffect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B0D76D35-FDB8-45CA-8D41-8D6C9597ED1B">SetAlphaDisable</a>
</td>
<td align="left" width="63%">
Specifies whether to apply the transfer function to the alpha channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn905291(v=VS.85).aspx">SetAlphaSlope</a>
</td>
<td align="left" width="63%">Overloaded. Sets the slope of the linear function for the alpha channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn905292(v=VS.85).aspx">SetAlphaYIntercept</a>
</td>
<td align="left" width="63%">Overloaded. Sets the Y-intercept of the linear function for the alpha channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DE87E53B-4469-4B30-8397-6A0712DE8A6C">SetBlueDisable</a>
</td>
<td align="left" width="63%">
Specifies whether to apply the transfer function to the blue channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn905293(v=VS.85).aspx">SetBlueSlope</a>
</td>
<td align="left" width="63%">Overloaded. The slope of the linear function for the blue channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn905294(v=VS.85).aspx">SetBlueYIntercept</a>
</td>
<td align="left" width="63%">Overloaded. Sets the Y-intercept of the linear function for the blue channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D56B3B15-6437-46A3-B1F9-88F5BC4A9BB2">SetClampOutput</a>
</td>
<td align="left" width="63%">
Specifies whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5C0C9E9C-F332-4F4E-A3F0-423A302AC6FC">SetGreenDisable</a>
</td>
<td align="left" width="63%">
Specifies whether to apply the transfer function to the green channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn905295(v=VS.85).aspx">setgreenslope</a>
</td>
<td align="left" width="63%">Overloaded. Sets the slope of the linear function for the green channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn905296(v=VS.85).aspx">SetGreenYIntercept</a>
</td>
<td align="left" width="63%">Overloaded. Sets the Y-intercept of the linear function for the green channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59B82C2B-9DAE-4B6C-A5ED-425A8ACEF24E">SetRedDisable</a>
</td>
<td align="left" width="63%">
Specifies whether to apply the transfer function to the red channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn905297(v=VS.85).aspx">setredslope</a>
</td>
<td align="left" width="63%">Overloaded. Sets the slope of the linear function for the red channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn905298(v=VS.85).aspx">SetRedYIntercept</a>
</td>
<td align="left" width="63%">Overloaded. Sets the Y-intercept of the linear function for the red channel.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4303c24d-e3e1-e188-bbef-e654c0e7e266">IDCompositionFilterEffect</a>
 

 

