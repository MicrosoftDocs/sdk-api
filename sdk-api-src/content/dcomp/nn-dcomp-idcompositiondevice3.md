---
UID: NN:dcomp.IDCompositionDevice3
title: IDCompositionDevice3
author: windows-sdk-content
description: Serves as a factory for all other Microsoft DirectComposition objects and provides methods to control transactional composition.
old-location: directcomp\idcompositiondevice3.htm
tech.root: directcomp
ms.assetid: 5da076dc-360d-0b28-f131-8669d1a91dd6
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IDCompositionDevice3, IDCompositionDevice3 interface [DirectComposition], IDCompositionDevice3 interface [DirectComposition],described, dcomp/IDCompositionDevice3, directcomp.idcompositiondevice3
ms.prod: windows
ms.technology: windows-sdk
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionDevice3</b> interface inherits from <a href="https://msdn.microsoft.com/0E5D0AEC-63A3-4A44-9A0B-D1E26789CAB0">IDCompositionDevice2</a>. <b>IDCompositionDevice3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/E7421DD7-0E7D-4DDC-A6CD-807BF8638E5B">CreateAffineTransform2DEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/1B693705-1118-4B9B-A7B7-E8811AE881AC">IDCompositionAffineTransform2DEffect</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0A06A546-7FD6-4B3C-86C8-0C5B9417D450">CreateArithmeticCompositeEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/06430DD6-B6BF-4F55-A99C-13860B800444">IDCompositionArithmeticCompositeEffect</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20E05261-E5B6-4F48-B595-F2AD8B96AB2E">CreateBlendEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/F8EDEA1D-A990-48C0-B4D4-3DD9261B47B2">IDCompositionBlendEffect</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4BD16F01-6CF1-4634-9D68-A153C7AABFFD">CreateBrightnessEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/22503D7B-A359-4877-A437-6A97D8835BC7">IDCompositionBrightnessEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A286F5C1-764F-4FAF-B2D2-92820BD2E709">CreateColorMatrixEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/75528E11-D041-4192-833A-31679316DF76">IDCompositionColorMatrixEffect</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9DA1541E-0792-482E-81AF-A6C91665D9D8">CreateCompositeEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/72647FCE-F1B0-4A50-927B-23EE38EEEC8B">IDCompositionCompositeEffect</a>.
        

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
<a href="https://msdn.microsoft.com/D05C7A70-107A-4246-9391-7B00ECAA0B80">CreateGaussianBlurEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/CFE79B69-75EC-4E22-BC3E-C82601AE1213">IDCompositionGaussianBlurEffect</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4DA99723-CC21-454B-A24A-3988A15861D2">CreateHueRotationEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/BD11C779-78C6-4961-9DF1-2521B8F91FF5">IDCompositionHueRotationEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C819B72A-ACE7-4201-9C4A-9D72E9E95FF7">CreateLinearTransferEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/516CD029-DBB1-4AD7-92BB-8B6EF6C733FA">IDCompositionLinearTransferEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19613AF4-6EC0-4918-9FC1-147A04D321CA">CreateSaturationEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/ADA7C54C-E237-4455-8808-962A631B37E0">IDCompositionSaturationEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C0A2B599-F061-4312-BDBC-96DF724F02D8">CreateShadowEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/115FD667-64D2-4538-9EB4-B133D5DCAF30">IDCompositionShadowEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C6438DB2-26DA-451A-B748-901C809C1369">CreateTableTransferEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/147E15B8-C529-4BC6-85AA-FB069B892C6C">IDCompositionTableTransferEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40BCD422-7545-4CB9-9C8E-2F0D2B4E6C51">CreateTurbulenceEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/6A0100DE-DB63-475C-BF7D-3B2D436704A5">IDCompositionTurbulenceEffect</a>.
        

</td>
</tr>
</table> 

