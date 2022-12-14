---
UID: NF:dcomp.IDCompositionShadowEffect.SetAlpha(IDCompositionAnimation)
title: IDCompositionShadowEffect::SetAlpha(IDCompositionAnimation) (dcomp.h)
description: Sets the alpha value for the effect. (overload 1/2)
helpviewer_keywords: ["IDCompositionShadowEffect interface [DirectComposition]","SetAlpha method","IDCompositionShadowEffect.SetAlpha","IDCompositionShadowEffect.SetAlpha(IDCompositionAnimation)","IDCompositionShadowEffect::SetAlpha","IDCompositionShadowEffect::SetAlpha(IDCompositionAnimation)","SetAlpha","SetAlpha method [DirectComposition]","SetAlpha method [DirectComposition]","IDCompositionShadowEffect interface","dcomp/IDCompositionShadowEffect::SetAlpha","directcomp.idcompositionshadoweffect_setalpha_2"]
old-location: directcomp\idcompositionshadoweffect_setalpha_2.htm
tech.root: directcomp
ms.assetid: 2C0C85FC-83AF-4036-9BCE-730457FB483F
ms.date: 12/05/2018
ms.keywords: IDCompositionShadowEffect interface [DirectComposition],SetAlpha method, IDCompositionShadowEffect.SetAlpha, IDCompositionShadowEffect.SetAlpha(IDCompositionAnimation), IDCompositionShadowEffect::SetAlpha, IDCompositionShadowEffect::SetAlpha(IDCompositionAnimation), SetAlpha, SetAlpha method [DirectComposition], SetAlpha method [DirectComposition],IDCompositionShadowEffect interface, dcomp/IDCompositionShadowEffect::SetAlpha, directcomp.idcompositionshadoweffect_setalpha_2
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
 - IDCompositionShadowEffect::SetAlpha
 - dcomp/IDCompositionShadowEffect::SetAlpha
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
 - IDCompositionShadowEffect.SetAlpha
---

# IDCompositionShadowEffect::SetAlpha(IDCompositionAnimation)


## -description

Sets the alpha value for the effect.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the alpha value for the effect changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionshadoweffect">IDCompositionShadowEffect</a>
