---
UID: NF:dcomp.IDCompositionSaturationEffect.SetSaturation(float)
title: IDCompositionSaturationEffect::SetSaturation(float) (dcomp.h)
description: Sets the saturation of the image. (overload 2/2)
helpviewer_keywords: ["IDCompositionSaturationEffect interface [DirectComposition]","SetSaturation method","IDCompositionSaturationEffect.SetSaturation","IDCompositionSaturationEffect.SetSaturation(float)","IDCompositionSaturationEffect::SetSaturation","IDCompositionSaturationEffect::SetSaturation(float)","SetSaturation","SetSaturation method [DirectComposition]","SetSaturation method [DirectComposition]","IDCompositionSaturationEffect interface","dcomp/IDCompositionSaturationEffect::SetSaturation","directcomp.idcompositionsaturationeffect_setsaturation"]
old-location: directcomp\idcompositionsaturationeffect_setsaturation.htm
tech.root: directcomp
ms.assetid: A2BAE19A-FC9F-4476-9DBB-438FE2923246
ms.date: 12/05/2018
ms.keywords: IDCompositionSaturationEffect interface [DirectComposition],SetSaturation method, IDCompositionSaturationEffect.SetSaturation, IDCompositionSaturationEffect.SetSaturation(float), IDCompositionSaturationEffect::SetSaturation, IDCompositionSaturationEffect::SetSaturation(float), SetSaturation, SetSaturation method [DirectComposition], SetSaturation method [DirectComposition],IDCompositionSaturationEffect interface, dcomp/IDCompositionSaturationEffect::SetSaturation, directcomp.idcompositionsaturationeffect_setsaturation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionSaturationEffect::SetSaturation
 - dcomp/IDCompositionSaturationEffect::SetSaturation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionSaturationEffect.SetSaturation
---

# IDCompositionSaturationEffect::SetSaturation(float)


## -description

Sets the saturation of the image.

## -parameters

### -param ratio [in]

Type: <b>float</b>

The saturation of the image. You can set the saturation to a value between 0 and 1. If you set it to 1 the output image is fully saturated. If you set it to 0 the output image is monochrome. The saturation value is unitless. The effect calculates a color matrix based on the saturation value (s in the equation here) using the following equation:
            
<img alt="Matrix equation" src="./images/saturation_formula.png"/>

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionsaturationeffect">IDCompositionSaturationEffect</a>
