---
UID: NF:dcomp.IDCompositionBrightnessEffect.SetWhitePoint
title: IDCompositionBrightnessEffect::SetWhitePoint
author: windows-sdk-content
description: Sets the upper portion of the brightness transfer curve.
old-location: directcomp\idcompositionbrightnesseffect_setwhitepoint.htm
tech.root: directcomp
ms.assetid: C06DFD2A-9B97-4254-BFB5-058FB0ED3F83
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IDCompositionBrightnessEffect interface [DirectComposition],SetWhitePoint method, IDCompositionBrightnessEffect.SetWhitePoint, IDCompositionBrightnessEffect::SetWhitePoint, SetWhitePoint, SetWhitePoint method [DirectComposition], SetWhitePoint method [DirectComposition],IDCompositionBrightnessEffect interface, dcomp/IDCompositionBrightnessEffect::SetWhitePoint, directcomp.idcompositionbrightnesseffect_setwhitepoint
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
 - IDCompositionBrightnessEffect.SetWhitePoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionBrightnessEffect::SetWhitePoint


## -description


Sets the upper portion of the brightness transfer curve. 


## -parameters




### -param whitePoint [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/DD180090-D2F4-4DF3-8652-101713C01AE4">D2D1_VECTOR_2F</a></b>

The upper portion of the brightness transfer curve. The white point adjusts the appearance of the brighter portions of the image. 
This vector is for both the x value and the y value, in that order. Each of the values must be between 0 and 1, inclusive.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/22503D7B-A359-4877-A437-6A97D8835BC7">IDCompositionBrightnessEffect</a>
 

 

