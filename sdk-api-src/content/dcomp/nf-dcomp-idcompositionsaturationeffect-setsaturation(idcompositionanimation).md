---
UID: NF:dcomp.IDCompositionSaturationEffect.SetSaturation(IDCompositionAnimation)
title: IDCompositionSaturationEffect::SetSaturation(IDCompositionAnimation)
author: windows-sdk-content
description: Sets the saturation of the image.
old-location: directcomp\idcompositionsaturationeffect_setsaturation.htm
tech.root: directcomp
ms.assetid: A2BAE19A-FC9F-4476-9DBB-438FE2923246
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IDCompositionSaturationEffect interface [DirectComposition],SetSaturation method, IDCompositionSaturationEffect.SetSaturation, IDCompositionSaturationEffect.SetSaturation(IDCompositionAnimation), IDCompositionSaturationEffect::SetSaturation, IDCompositionSaturationEffect::SetSaturation(IDCompositionAnimation), SetSaturation, SetSaturation method [DirectComposition], SetSaturation method [DirectComposition],IDCompositionSaturationEffect interface, dcomp/IDCompositionSaturationEffect::SetSaturation, directcomp.idcompositionsaturationeffect_setsaturation
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
 - IDCompositionSaturationEffect.SetSaturation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionSaturationEffect::SetSaturation(IDCompositionAnimation)


## -description


Sets the saturation of the image.


## -parameters




### -param animation

TBD




#### - ratio [in]

Type: <b>float</b>

The saturation of the image. You can set the saturation to a value between 0 and 1. If you set it to 1 the output image is fully saturated.
            If you set it to 0 the output image is monochrome. The saturation value is unitless.
            
            The effect calculates a color matrix based on the saturation value (s in the equation here) using the following equation:
            

<img alt="Matrix equation" src="images/saturation_formula.png"/>

## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ADA7C54C-E237-4455-8808-962A631B37E0">IDCompositionSaturationEffect</a>
 

 

