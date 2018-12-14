---
UID: NN:dcomp.IDCompositionDevice3
title: IDCompositionDevice3
author: windows-sdk-content
description: Serves as a factory for all other Microsoft DirectComposition objects and provides methods to control transactional composition.
old-location: directcomp\idcompositiondevice3.htm
tech.root: directcomp
ms.assetid: 5da076dc-360d-0b28-f131-8669d1a91dd6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionDevice3, IDCompositionDevice3 interface [DirectComposition], IDCompositionDevice3 interface [DirectComposition],described, dcomp/IDCompositionDevice3, directcomp.idcompositiondevice3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDCompositionDevice3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice3 interface


## -description


Serves as a factory for all other Microsoft DirectComposition objects and provides methods to control transactional composition.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionDevice3</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dn280354(v=VS.85).aspx">IDCompositionDevice2</a>. <b>IDCompositionDevice3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionDevice3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn950127(v=VS.85).aspx">CreateAffineTransform2DEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/en-us/library/Dn919690(v=VS.85).aspx">IDCompositionAffineTransform2DEffect</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn950128(v=VS.85).aspx">CreateArithmeticCompositeEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/en-us/library/Dn919698(v=VS.85).aspx">IDCompositionArithmeticCompositeEffect</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn950129(v=VS.85).aspx">CreateBlendEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/en-us/library/Dn919709(v=VS.85).aspx">IDCompositionBlendEffect</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn950130(v=VS.85).aspx">CreateBrightnessEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/en-us/library/Dn919711(v=VS.85).aspx">IDCompositionBrightnessEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn950131(v=VS.85).aspx">CreateColorMatrixEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/en-us/library/Dn919722(v=VS.85).aspx">IDCompositionColorMatrixEffect</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn950132(v=VS.85).aspx">CreateCompositeEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/en-us/library/Dn919728(v=VS.85).aspx">IDCompositionCompositeEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04DBF317-CF21-4D66-AE46-BD0A42F12522">CreateFloodEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/A8A3ACF1-D074-454E-8F48-E5110A49CCD3">IDCompositionFloodEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn950134(v=VS.85).aspx">CreateGaussianBlurEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/en-us/library/Dn919734(v=VS.85).aspx">IDCompositionGaussianBlurEffect</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn950135(v=VS.85).aspx">CreateHueRotationEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/en-us/library/Dn919738(v=VS.85).aspx">IDCompositionHueRotationEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn950136(v=VS.85).aspx">CreateLinearTransferEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/en-us/library/Dn919741(v=VS.85).aspx">IDCompositionLinearTransferEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn950137(v=VS.85).aspx">CreateSaturationEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/en-us/library/Dn919763(v=VS.85).aspx">IDCompositionSaturationEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn950138(v=VS.85).aspx">CreateShadowEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/en-us/library/Dn919766(v=VS.85).aspx">IDCompositionShadowEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn950139(v=VS.85).aspx">CreateTableTransferEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/en-us/library/Dn919783(v=VS.85).aspx">IDCompositionTableTransferEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn950140(v=VS.85).aspx">CreateTurbulenceEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/en-us/library/Dn919801(v=VS.85).aspx">IDCompositionTurbulenceEffect</a>.
        

</td>
</tr>
</table> 

