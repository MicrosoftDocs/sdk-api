---
UID: NF:dcomp.IDCompositionShadowEffect.SetStandardDeviation(IDCompositionAnimation)
title: IDCompositionShadowEffect::SetStandardDeviation(IDCompositionAnimation) (dcomp.h)
description: Sets the amount of blur to be applied to the alpha channel of the image. (overload 2/2)
helpviewer_keywords: ["IDCompositionShadowEffect interface [DirectComposition]","SetStandardDeviation method","IDCompositionShadowEffect.SetStandardDeviation","IDCompositionShadowEffect.SetStandardDeviation(IDCompositionAnimation)","IDCompositionShadowEffect::SetStandardDeviation","IDCompositionShadowEffect::SetStandardDeviation(IDCompositionAnimation)","SetStandardDeviation","SetStandardDeviation method [DirectComposition]","SetStandardDeviation method [DirectComposition]","IDCompositionShadowEffect interface","dcomp/IDCompositionShadowEffect::SetStandardDeviation","directcomp.idcompositionshadoweffect_setstandarddeviation_2"]
old-location: directcomp\idcompositionshadoweffect_setstandarddeviation_2.htm
tech.root: directcomp
ms.assetid: B5470CF6-A24B-4168-904E-2465372B60FC
ms.date: 12/05/2018
ms.keywords: IDCompositionShadowEffect interface [DirectComposition],SetStandardDeviation method, IDCompositionShadowEffect.SetStandardDeviation, IDCompositionShadowEffect.SetStandardDeviation(IDCompositionAnimation), IDCompositionShadowEffect::SetStandardDeviation, IDCompositionShadowEffect::SetStandardDeviation(IDCompositionAnimation), SetStandardDeviation, SetStandardDeviation method [DirectComposition], SetStandardDeviation method [DirectComposition],IDCompositionShadowEffect interface, dcomp/IDCompositionShadowEffect::SetStandardDeviation, directcomp.idcompositionshadoweffect_setstandarddeviation_2
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
 - IDCompositionShadowEffect::SetStandardDeviation
 - dcomp/IDCompositionShadowEffect::SetStandardDeviation
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
 - IDCompositionShadowEffect.SetStandardDeviation
---

# IDCompositionShadowEffect::SetStandardDeviation(IDCompositionAnimation)


## -description

Sets the amount of blur to be applied to the alpha channel of the image.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the amount of blur to be applied to the alpha channel of the image changes over time. 
            You can compute the blur radius of the kernel by multiplying the standard deviation by 3.
            The units of both the standard deviation and blur radius are DIPs.          
          This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionshadoweffect">IDCompositionShadowEffect</a>
