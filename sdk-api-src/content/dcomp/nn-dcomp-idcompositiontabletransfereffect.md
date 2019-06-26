---
UID: NN:dcomp.IDCompositionTableTransferEffect
title: IDCompositionTableTransferEffect (dcomp.h)
author: windows-sdk-content
description: The table transfer effect is used to map the color intensities of an image using a transfer function created from interpolating a list of values you provide.
old-location: directcomp\idcompositiontabletransfereffect.htm
tech.root: directcomp
ms.assetid: 147E15B8-C529-4BC6-85AA-FB069B892C6C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionTableTransferEffect, IDCompositionTableTransferEffect interface [DirectComposition], IDCompositionTableTransferEffect interface [DirectComposition],described, dcomp/IDCompositionTableTransferEffect, directcomp.idcompositiontabletransfereffect
ms.topic: interface
f1_keywords: 
 - "dcomp/IDCompositionTableTransferEffect"
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
ms.custom: 19H1
---

# IDCompositionTableTransferEffect interface


## -description


The table transfer effect is used to map the color intensities of an image using a transfer function created from interpolating a list of values you provide.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionTableTransferEffect</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionfiltereffect">IDCompositionFilterEffect</a>. <b>IDCompositionTableTransferEffect</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiontabletransfereffect-setalphadisable">SetAlphaDisable</a>
</td>
<td align="left" width="63%">
Specifies whether to apply the transfer function to the Alpha channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiontabletransfereffect-setalphatable">SetAlphaTable</a>
</td>
<td align="left" width="63%">
Sets the list of values used to define the transfer function for the alpha channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setalphatablevalue">SetAlphaTableValue</a>
</td>
<td align="left" width="63%">Overloaded. Sets a value in the alpha table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiontabletransfereffect-setbluedisable">SetBlueDisable</a>
</td>
<td align="left" width="63%">
Specifies whether to apply the transfer function to the blue channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiontabletransfereffect-setbluetable">SetBlueTable</a>
</td>
<td align="left" width="63%">
Sets the list of values used to define the transfer function for the blue channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setbluetablevalue">SetBlueTableValue</a>
</td>
<td align="left" width="63%">Overloaded. Sets a value in the blue table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiontabletransfereffect-setclampoutput">SetClampOutput</a>
</td>
<td align="left" width="63%">
Specifies whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiontabletransfereffect-setgreendisable">SetGreenDisable</a>
</td>
<td align="left" width="63%">
Specifies whether to apply the transfer function to the green channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiontabletransfereffect-setgreentable">SetGreenTable</a>
</td>
<td align="left" width="63%">
Sets the list of values used to define the transfer function for the green channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setgreentablevalue">SetGreenTableValue</a>
</td>
<td align="left" width="63%">Overloaded. Sets a value in the green table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiontabletransfereffect-setreddisable">SetRedDisable</a>
</td>
<td align="left" width="63%">
Specifies whether to apply the transfer function to the red channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiontabletransfereffect-setredtable">SetRedTable</a>
</td>
<td align="left" width="63%">
Sets the list of values used to define the transfer function for the red channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setredtablevalue">SetRedTableValue</a>
</td>
<td align="left" width="63%">Overloaded. Sets a value in the red table.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionfiltereffect">IDCompositionFilterEffect</a>
 

 

