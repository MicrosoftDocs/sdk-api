---
UID: NN:dcomp.IDCompositionTableTransferEffect
title: IDCompositionTableTransferEffect
author: windows-sdk-content
description: The table transfer effect is used to map the color intensities of an image using a transfer function created from interpolating a list of values you provide.
old-location: directcomp\idcompositiontabletransfereffect.htm
tech.root: directcomp
ms.assetid: 147E15B8-C529-4BC6-85AA-FB069B892C6C
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IDCompositionTableTransferEffect, IDCompositionTableTransferEffect interface [DirectComposition], IDCompositionTableTransferEffect interface [DirectComposition],described, dcomp/IDCompositionTableTransferEffect, directcomp.idcompositiontabletransfereffect
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
 - IDCompositionTableTransferEffect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionTableTransferEffect interface


## -description


The table transfer effect is used to map the color intensities of an image using a transfer function created from interpolating a list of values you provide.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionTableTransferEffect</b> interface inherits from <a href="https://msdn.microsoft.com/4303c24d-e3e1-e188-bbef-e654c0e7e266">IDCompositionFilterEffect</a>. <b>IDCompositionTableTransferEffect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionTableTransferEffect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BC05E32A-787C-4472-8C18-D21D32324373">SetAlphaDisable</a>
</td>
<td align="left" width="63%">
Specifies whether to apply the transfer function to the Alpha channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8CF6673B-9D9C-40B9-AC91-B2F63450FE64">SetAlphaTable</a>
</td>
<td align="left" width="63%">
Sets the list of values used to define the transfer function for the alpha channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f4e04e0-1ec6-a475-264e-d64f68e23fb9">SetAlphaTableValue</a>
</td>
<td align="left" width="63%">Overloaded. Sets a value in the alpha table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/278FE30E-86F2-4E34-AED5-78C699FC2319">SetBlueDisable</a>
</td>
<td align="left" width="63%">
Specifies whether to apply the transfer function to the blue channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D6E5D8CB-8E69-4E33-AC2E-4995F9D4283A">SetBlueTable</a>
</td>
<td align="left" width="63%">
Sets the list of values used to define the transfer function for the blue channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c7098d5-17aa-3154-02a7-7acf972a212d">SetBlueTableValue</a>
</td>
<td align="left" width="63%">Overloaded. Sets a value in the blue table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6F1A7757-92DA-4BDC-9894-7A8906461FD5">SetClampOutput</a>
</td>
<td align="left" width="63%">
Specifies whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C625ACED-C8E8-414D-A9E9-4119F8F1D434">SetGreenDisable</a>
</td>
<td align="left" width="63%">
Specifies whether to apply the transfer function to the green channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90FB09CA-EC67-4518-915E-223C26E30FA4">SetGreenTable</a>
</td>
<td align="left" width="63%">
Sets the list of values used to define the transfer function for the green channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/feccfc61-31e6-362a-1e81-0650736b962a">SetGreenTableValue</a>
</td>
<td align="left" width="63%">Overloaded. Sets a value in the green table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9CDE9200-F5AF-47AB-9B79-8602188FF4CA">SetRedDisable</a>
</td>
<td align="left" width="63%">
Specifies whether to apply the transfer function to the red channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4113919E-84B9-402A-A2A1-64EB74D2CC59">SetRedTable</a>
</td>
<td align="left" width="63%">
Sets the list of values used to define the transfer function for the red channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cfa766c-b88d-9a8f-109f-b42e9df79cbf">SetRedTableValue</a>
</td>
<td align="left" width="63%">Overloaded. Sets a value in the red table.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4303c24d-e3e1-e188-bbef-e654c0e7e266">IDCompositionFilterEffect</a>
 

 

