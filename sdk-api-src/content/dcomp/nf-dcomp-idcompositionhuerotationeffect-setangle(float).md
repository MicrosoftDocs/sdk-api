---
UID: NF:dcomp.IDCompositionHueRotationEffect.SetAngle(float)
title: IDCompositionHueRotationEffect::SetAngle(float)
author: windows-sdk-content
description: Sets the angle to rotate the hue.
old-location: directcomp\idcompositionhuerotationeffect_setangle.htm
tech.root: directcomp
ms.assetid: BA98A918-EE51-40C7-9392-D5E0D78580F8
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDCompositionHueRotationEffect interface [DirectComposition],SetAngle method, IDCompositionHueRotationEffect.SetAngle, IDCompositionHueRotationEffect.SetAngle(float), IDCompositionHueRotationEffect::SetAngle, IDCompositionHueRotationEffect::SetAngle(float), SetAngle, SetAngle method [DirectComposition], SetAngle method [DirectComposition],IDCompositionHueRotationEffect interface, dcomp/IDCompositionHueRotationEffect::SetAngle, directcomp.idcompositionhuerotationeffect_setangle
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
 - IDCompositionHueRotationEffect.SetAngle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dcomp.h
: 
- IDCompositionHueRotationEffect.SetAngle
: 
---

# IDCompositionHueRotationEffect::SetAngle(float)


## -description


Sets the angle to rotate the hue.


## -parameters




### -param amountDegrees [in]

Type: <b>float</b>

The angle to rotate the hue. The effect calculates a color matrix based on the rotation angle (θ) according to the following matrix equations:
          

<img alt="Matrix equation" src="./images/hue_formula.png"/>

## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/BD11C779-78C6-4961-9DF1-2521B8F91FF5">IDCompositionHueRotationEffect</a>
 

 

