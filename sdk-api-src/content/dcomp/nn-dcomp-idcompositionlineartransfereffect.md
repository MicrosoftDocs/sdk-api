---
UID: NN:dcomp.IDCompositionLinearTransferEffect
title: IDCompositionLinearTransferEffect
author: windows-sdk-content
description: The linear transfer effect is used to map the color intensities of an image using a linear function created from a list of values you provide for each channel.
old-location: directcomp\idcompositionlineartransfereffect.htm
tech.root: directcomp
ms.assetid: 516CD029-DBB1-4AD7-92BB-8B6EF6C733FA
ms.author: windowssdkdev
ms.date: 12/5/2018
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
---

# IDCompositionLinearTransferEffect interface


## -description


The linear transfer effect is used to map the color intensities of an image using a linear function created from a list of values you provide for each channel.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionLinearTransferEffect</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dn919730(v=VS.85).aspx">IDCompositionFilterEffect</a>. <b>IDCompositionLinearTransferEffect</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dn919742(v=VS.85).aspx">SetAlphaDisable</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Dn919747(v=VS.85).aspx">SetBlueDisable</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Dn919752(v=VS.85).aspx">SetClampOutput</a>
</td>
<td align="left" width="63%">
Specifies whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn919753(v=VS.85).aspx">SetGreenDisable</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Dn919758(v=VS.85).aspx">SetRedDisable</a>
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




<a href="https://msdn.microsoft.com/en-us/library/Dn919730(v=VS.85).aspx">IDCompositionFilterEffect</a>
 

 

