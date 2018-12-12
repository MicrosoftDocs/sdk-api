---
UID: NF:dcomp.IDCompositionFilterEffect.SetInput
title: IDCompositionFilterEffect::SetInput
author: windows-sdk-content
description: Sets the the input at an index to the specified filter effect.
old-location: directcomp\idcompositionfiltereffect_setinput.htm
tech.root: directcomp
ms.assetid: 8DFF137E-2979-42D4-A8A5-F831A33468CA
ms.author: windowssdkdev
ms.date: 12/5/2018
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
<a href="https://msdn.microsoft.com/en-us/library/Dn919690(v=VS.85).aspx">IDCompositionAffineTransform2DEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn919698(v=VS.85).aspx">IDCompositionArithmeticCompositeEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn919709(v=VS.85).aspx">IDCompositionBlendEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn919711(v=VS.85).aspx">IDCompositionBrightnessEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn919722(v=VS.85).aspx">IDCompositionColorNatrixEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn919728(v=VS.85).aspx">IDCompositionCompositeEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A8A3ACF1-D074-454E-8F48-E5110A49CCD3">IDCompositionFloodEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn919734(v=VS.85).aspx">IDCompositionGaussianBlurEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn919738(v=VS.85).aspx">IDCompositionHueRotationEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn919741(v=VS.85).aspx">IDCompositionLinearTransferRffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn919763(v=VS.85).aspx">IDCompositionSaturationRffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn919766(v=VS.85).aspx">IDCompositionShadowEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn919783(v=VS.85).aspx">IDCompositionTableTransferEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn919801(v=VS.85).aspx">IDCompositionTurbulenceEffect</a>
</li>
</ul>

### -param flags [in]

Type: <b>UINT</b>

Flags to apply to the filter effect. 
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn919730(v=VS.85).aspx">IDCompositionFilterEffect</a>
 

 

