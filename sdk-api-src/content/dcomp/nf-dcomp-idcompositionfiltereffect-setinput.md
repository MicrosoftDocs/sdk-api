---
UID: NF:dcomp.IDCompositionFilterEffect.SetInput
title: IDCompositionFilterEffect::SetInput
author: windows-sdk-content
description: Sets the the input at an index to the specified filter effect.
old-location: directcomp\idcompositionfiltereffect_setinput.htm
tech.root: directcomp
ms.assetid: 8DFF137E-2979-42D4-A8A5-F831A33468CA
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IDCompositionFilterEffect interface [DirectComposition],SetInput method, IDCompositionFilterEffect.SetInput, IDCompositionFilterEffect::SetInput, SetInput, SetInput method [DirectComposition], SetInput method [DirectComposition],IDCompositionFilterEffect interface, dcomp/IDCompositionFilterEffect::SetInput, directcomp.idcompositionfiltereffect_setinput
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDCompositionFilterEffect.SetInput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionFilterEffect::SetInput


## -description


Sets the the input at an index to the specified filter effect.


## -parameters




### -param index [in]

Type: <b>UINT</b>

Specifies the index the to apply the filter effect at.


### -param input [in, optional]

Type: <b>IUnknown*</b>

The filter effect to apply.
          The following effects are available:
          

<ul>
<li>
<a href="https://msdn.microsoft.com/1B693705-1118-4B9B-A7B7-E8811AE881AC">IDCompositionAffineTransform2DEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/06430DD6-B6BF-4F55-A99C-13860B800444">IDCompositionArithmeticCompositeEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/F8EDEA1D-A990-48C0-B4D4-3DD9261B47B2">IDCompositionBlendEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/22503D7B-A359-4877-A437-6A97D8835BC7">IDCompositionBrightnessEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/75528E11-D041-4192-833A-31679316DF76">IDCompositionColorNatrixEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/72647FCE-F1B0-4A50-927B-23EE38EEEC8B">IDCompositionCompositeEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A8A3ACF1-D074-454E-8F48-E5110A49CCD3">IDCompositionFloodEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/CFE79B69-75EC-4E22-BC3E-C82601AE1213">IDCompositionGaussianBlurEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/BD11C779-78C6-4961-9DF1-2521B8F91FF5">IDCompositionHueRotationEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/516CD029-DBB1-4AD7-92BB-8B6EF6C733FA">IDCompositionLinearTransferRffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ADA7C54C-E237-4455-8808-962A631B37E0">IDCompositionSaturationRffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/115FD667-64D2-4538-9EB4-B133D5DCAF30">IDCompositionShadowEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/147E15B8-C529-4BC6-85AA-FB069B892C6C">IDCompositionTableTransferEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6A0100DE-DB63-475C-BF7D-3B2D436704A5">IDCompositionTurbulenceEffect</a>
</li>
</ul>

### -param flags [in]

Type: <b>UINT</b>

Flags to apply to the filter effect. 
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4303c24d-e3e1-e188-bbef-e654c0e7e266">IDCompositionFilterEffect</a>
 

 

