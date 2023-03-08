---
UID: NF:dcomp.IDCompositionShadowEffect.SetBlue(IDCompositionAnimation)
title: IDCompositionShadowEffect::SetBlue(IDCompositionAnimation) (dcomp.h)
description: Sets the blue value for the color of the shadow. (overload 2/2)
helpviewer_keywords: ["IDCompositionShadowEffect interface [DirectComposition]","SetBlue method","IDCompositionShadowEffect.SetBlue","IDCompositionShadowEffect.SetBlue(IDCompositionAnimation)","IDCompositionShadowEffect::SetBlue","IDCompositionShadowEffect::SetBlue(IDCompositionAnimation)","SetBlue","SetBlue method [DirectComposition]","SetBlue method [DirectComposition]","IDCompositionShadowEffect interface","dcomp/IDCompositionShadowEffect::SetBlue","directcomp.idcompositionshadoweffect_setblue_2"]
old-location: directcomp\idcompositionshadoweffect_setblue_2.htm
tech.root: directcomp
ms.assetid: DE146FA2-FB55-4588-82CB-C6E6BD2DB71E
ms.date: 12/05/2018
ms.keywords: IDCompositionShadowEffect interface [DirectComposition],SetBlue method, IDCompositionShadowEffect.SetBlue, IDCompositionShadowEffect.SetBlue(IDCompositionAnimation), IDCompositionShadowEffect::SetBlue, IDCompositionShadowEffect::SetBlue(IDCompositionAnimation), SetBlue, SetBlue method [DirectComposition], SetBlue method [DirectComposition],IDCompositionShadowEffect interface, dcomp/IDCompositionShadowEffect::SetBlue, directcomp.idcompositionshadoweffect_setblue_2
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
 - IDCompositionShadowEffect::SetBlue
 - dcomp/IDCompositionShadowEffect::SetBlue
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
 - IDCompositionShadowEffect.SetBlue
---

# IDCompositionShadowEffect::SetBlue(IDCompositionAnimation)


## -description

Sets the blue value for the color of the shadow.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the blue value for the color of the shadow changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionshadoweffect">IDCompositionShadowEffect</a>
