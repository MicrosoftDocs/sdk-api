---
UID: NF:dcomp.IDCompositionBrightnessEffect.SetBlackPointX(IDCompositionAnimation)
title: IDCompositionBrightnessEffect::SetBlackPointX(IDCompositionAnimation) (dcomp.h)
description: Sets the x value of the black point. (overload 1/2)
helpviewer_keywords: ["IDCompositionBrightnessEffect interface [DirectComposition]","SetBlackPointX method","IDCompositionBrightnessEffect.SetBlackPointX","IDCompositionBrightnessEffect.SetBlackPointX(IDCompositionAnimation)","IDCompositionBrightnessEffect::SetBlackPointX","IDCompositionBrightnessEffect::SetBlackPointX(IDCompositionAnimation)","SetBlackPointX","SetBlackPointX method [DirectComposition]","SetBlackPointX method [DirectComposition]","IDCompositionBrightnessEffect interface","dcomp/IDCompositionBrightnessEffect::SetBlackPointX","directcomp.idcompositionbrightnesseffect_setblackpointx_2"]
old-location: directcomp\idcompositionbrightnesseffect_setblackpointx_2.htm
tech.root: directcomp
ms.assetid: E575DB19-9C28-4C4F-9339-16F562542D32
ms.date: 12/05/2018
ms.keywords: IDCompositionBrightnessEffect interface [DirectComposition],SetBlackPointX method, IDCompositionBrightnessEffect.SetBlackPointX, IDCompositionBrightnessEffect.SetBlackPointX(IDCompositionAnimation), IDCompositionBrightnessEffect::SetBlackPointX, IDCompositionBrightnessEffect::SetBlackPointX(IDCompositionAnimation), SetBlackPointX, SetBlackPointX method [DirectComposition], SetBlackPointX method [DirectComposition],IDCompositionBrightnessEffect interface, dcomp/IDCompositionBrightnessEffect::SetBlackPointX, directcomp.idcompositionbrightnesseffect_setblackpointx_2
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
 - IDCompositionBrightnessEffect::SetBlackPointX
 - dcomp/IDCompositionBrightnessEffect::SetBlackPointX
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
 - IDCompositionBrightnessEffect.SetBlackPointX
---

# IDCompositionBrightnessEffect::SetBlackPointX(IDCompositionAnimation)


## -description

Sets the x value of the black point.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the x value of the black point changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionbrightnesseffect">IDCompositionBrightnessEffect</a>
