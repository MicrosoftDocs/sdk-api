---
UID: NF:dcomp.IDCompositionSaturationEffect.SetSaturation(IDCompositionAnimation)
title: IDCompositionSaturationEffect::SetSaturation(IDCompositionAnimation) (dcomp.h)
description: Sets the saturation of the image. (overload 1/2)
helpviewer_keywords: ["IDCompositionSaturationEffect interface [DirectComposition]","SetSaturation method","IDCompositionSaturationEffect.SetSaturation","IDCompositionSaturationEffect.SetSaturation(IDCompositionAnimation)","IDCompositionSaturationEffect::SetSaturation","IDCompositionSaturationEffect::SetSaturation(IDCompositionAnimation)","SetSaturation","SetSaturation method [DirectComposition]","SetSaturation method [DirectComposition]","IDCompositionSaturationEffect interface","dcomp/IDCompositionSaturationEffect::SetSaturation","directcomp.idcompositionsaturationeffect_setsaturation_2"]
old-location: directcomp\idcompositionsaturationeffect_setsaturation_2.htm
tech.root: directcomp
ms.assetid: 0F206128-A0F2-4BE3-A22D-2BAA8853099C
ms.date: 12/05/2018
ms.keywords: IDCompositionSaturationEffect interface [DirectComposition],SetSaturation method, IDCompositionSaturationEffect.SetSaturation, IDCompositionSaturationEffect.SetSaturation(IDCompositionAnimation), IDCompositionSaturationEffect::SetSaturation, IDCompositionSaturationEffect::SetSaturation(IDCompositionAnimation), SetSaturation, SetSaturation method [DirectComposition], SetSaturation method [DirectComposition],IDCompositionSaturationEffect interface, dcomp/IDCompositionSaturationEffect::SetSaturation, directcomp.idcompositionsaturationeffect_setsaturation_2
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

# IDCompositionSaturationEffect::SetSaturation(IDCompositionAnimation)


## -description

Sets the saturation of the image.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the saturation of the image changes over time. This parameter must not be NULL. You can set the saturation to a value between 0 and 1. If you set it to 1 the output image is fully saturated. If you set it to 0 the output image is monochrome. The saturation value is unitless. The effect calculates a color matrix based on the saturation value (s in the equation here) using the following equation:
            
<img alt="Matrix equation" src="./images/saturation_formula.png"/>

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionsaturationeffect">IDCompositionSaturationEffect</a>
