---
UID: NF:dcomp.IDCompositionShadowEffect.SetRed(IDCompositionAnimation)
title: IDCompositionShadowEffect::SetRed(IDCompositionAnimation) (dcomp.h)
description: Sets the red value for the color of the shadow. (overload 1/2)
helpviewer_keywords: ["IDCompositionShadowEffect interface [DirectComposition]","SetRed method","IDCompositionShadowEffect.SetRed","IDCompositionShadowEffect.SetRed(IDCompositionAnimation)","IDCompositionShadowEffect::SetRed","IDCompositionShadowEffect::SetRed(IDCompositionAnimation)","SetRed","SetRed method [DirectComposition]","SetRed method [DirectComposition]","IDCompositionShadowEffect interface","dcomp/IDCompositionShadowEffect::SetRed","directcomp.idcompositionshadoweffect_setred_2"]
old-location: directcomp\idcompositionshadoweffect_setred_2.htm
tech.root: directcomp
ms.assetid: 91440FC9-DCDA-44F1-B227-56A628686272
ms.date: 12/05/2018
ms.keywords: IDCompositionShadowEffect interface [DirectComposition],SetRed method, IDCompositionShadowEffect.SetRed, IDCompositionShadowEffect.SetRed(IDCompositionAnimation), IDCompositionShadowEffect::SetRed, IDCompositionShadowEffect::SetRed(IDCompositionAnimation), SetRed, SetRed method [DirectComposition], SetRed method [DirectComposition],IDCompositionShadowEffect interface, dcomp/IDCompositionShadowEffect::SetRed, directcomp.idcompositionshadoweffect_setred_2
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
 - IDCompositionShadowEffect::SetRed
 - dcomp/IDCompositionShadowEffect::SetRed
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
 - IDCompositionShadowEffect.SetRed
---

# IDCompositionShadowEffect::SetRed(IDCompositionAnimation)


## -description

Sets the red value for the color of the shadow.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the red value for the color of the shadow changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionshadoweffect">IDCompositionShadowEffect</a>
