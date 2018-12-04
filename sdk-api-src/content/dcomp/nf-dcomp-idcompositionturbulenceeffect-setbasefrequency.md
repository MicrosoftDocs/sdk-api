---
UID: NF:dcomp.IDCompositionTurbulenceEffect.SetBaseFrequency
title: IDCompositionTurbulenceEffect::SetBaseFrequency
author: windows-sdk-content
description: Sets the base frequencies in the X and Y direction.
old-location: directcomp\idcompositionturbulenceeffect_setbasefrequency.htm
tech.root: directcomp
ms.assetid: 4231DC9C-3CF3-405C-80BB-6DABCA40B4CD
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IDCompositionTurbulenceEffect interface [DirectComposition],SetBaseFrequency method, IDCompositionTurbulenceEffect.SetBaseFrequency, IDCompositionTurbulenceEffect::SetBaseFrequency, SetBaseFrequency, SetBaseFrequency method [DirectComposition], SetBaseFrequency method [DirectComposition],IDCompositionTurbulenceEffect interface, dcomp/IDCompositionTurbulenceEffect::SetBaseFrequency, directcomp.idcompositionturbulenceeffect_setbasefrequency
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
 - IDCompositionTurbulenceEffect.SetBaseFrequency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionTurbulenceEffect::SetBaseFrequency


## -description


Sets the base frequencies in the X and Y direction.


## -parameters




### -param frequency [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/DD180090-D2F4-4DF3-8652-101713C01AE4">D2D1_VECTOR_2F</a></b>

The base frequencies in the X and Y direction. This must be greater than 0. The units are specified in 1/DIPs.
            A value of 1 (1/DIPs) for the base frequency results in the Perlin noise completing an entire cycle between two pixels. The ease interpolation for these pixels results in completely random pixels,
            since there is no correlation between the pixels.
            A value of 0.1(1/DIPs) for the base frequency results in the Perlin noise function repeating every 10 DIPs. This results in correlation between pixels and the typical turbulence effect is visible.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6A0100DE-DB63-475C-BF7D-3B2D436704A5">IDCompositionTurbulenceEffect</a>
 

 

