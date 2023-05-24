---
UID: NF:dcomp.IDCompositionBrightnessEffect.SetBlackPointY(IDCompositionAnimation)
title: IDCompositionBrightnessEffect::SetBlackPointY(IDCompositionAnimation) (dcomp.h)
description: Sets the y value of the black point. (overload 2/2)
helpviewer_keywords: ["IDCompositionBrightnessEffect interface [DirectComposition]","SetBlackPointY method","IDCompositionBrightnessEffect.SetBlackPointY","IDCompositionBrightnessEffect.SetBlackPointY(IDCompositionAnimation)","IDCompositionBrightnessEffect::SetBlackPointY","IDCompositionBrightnessEffect::SetBlackPointY(IDCompositionAnimation)","SetBlackPointY","SetBlackPointY method [DirectComposition]","SetBlackPointY method [DirectComposition]","IDCompositionBrightnessEffect interface","dcomp/IDCompositionBrightnessEffect::SetBlackPointY","directcomp.idcompositionbrightnesseffect_setblackpointy_2"]
old-location: directcomp\idcompositionbrightnesseffect_setblackpointy_2.htm
tech.root: directcomp
ms.assetid: 3469E62F-4DAF-4FC7-9BBE-3B246260B1D5
ms.date: 12/05/2018
ms.keywords: IDCompositionBrightnessEffect interface [DirectComposition],SetBlackPointY method, IDCompositionBrightnessEffect.SetBlackPointY, IDCompositionBrightnessEffect.SetBlackPointY(IDCompositionAnimation), IDCompositionBrightnessEffect::SetBlackPointY, IDCompositionBrightnessEffect::SetBlackPointY(IDCompositionAnimation), SetBlackPointY, SetBlackPointY method [DirectComposition], SetBlackPointY method [DirectComposition],IDCompositionBrightnessEffect interface, dcomp/IDCompositionBrightnessEffect::SetBlackPointY, directcomp.idcompositionbrightnesseffect_setblackpointy_2
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
 - IDCompositionBrightnessEffect::SetBlackPointY
 - dcomp/IDCompositionBrightnessEffect::SetBlackPointY
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
 - IDCompositionBrightnessEffect.SetBlackPointY
---

# IDCompositionBrightnessEffect::SetBlackPointY(IDCompositionAnimation)


## -description

Sets the y value of the black point.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the y value of the black point changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionbrightnesseffect">IDCompositionBrightnessEffect</a>
