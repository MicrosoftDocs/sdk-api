---
UID: NF:dcomp.IDCompositionShadowEffect.SetStandardDeviation(float)
title: IDCompositionShadowEffect::SetStandardDeviation(float) (dcomp.h)
description: Sets the amount of blur to be applied to the alpha channel of the image. (overload 1/2)
helpviewer_keywords: ["IDCompositionShadowEffect interface [DirectComposition]","SetStandardDeviation method","IDCompositionShadowEffect.SetStandardDeviation","IDCompositionShadowEffect.SetStandardDeviation(float)","IDCompositionShadowEffect::SetStandardDeviation","IDCompositionShadowEffect::SetStandardDeviation(float)","SetStandardDeviation","SetStandardDeviation method [DirectComposition]","SetStandardDeviation method [DirectComposition]","IDCompositionShadowEffect interface","dcomp/IDCompositionShadowEffect::SetStandardDeviation","directcomp.idcompositionshadoweffect_setstandarddeviation"]
old-location: directcomp\idcompositionshadoweffect_setstandarddeviation.htm
tech.root: directcomp
ms.assetid: 5860E4F6-D778-4F10-ACE1-416E6D378528
ms.date: 12/05/2018
ms.keywords: IDCompositionShadowEffect interface [DirectComposition],SetStandardDeviation method, IDCompositionShadowEffect.SetStandardDeviation, IDCompositionShadowEffect.SetStandardDeviation(float), IDCompositionShadowEffect::SetStandardDeviation, IDCompositionShadowEffect::SetStandardDeviation(float), SetStandardDeviation, SetStandardDeviation method [DirectComposition], SetStandardDeviation method [DirectComposition],IDCompositionShadowEffect interface, dcomp/IDCompositionShadowEffect::SetStandardDeviation, directcomp.idcompositionshadoweffect_setstandarddeviation
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

# IDCompositionShadowEffect::SetStandardDeviation(float)


## -description

Sets the amount of blur to be applied to the alpha channel of the image.

## -parameters

### -param amount [in]

Type: <b>float</b>

The amount of blur to be applied to the alpha channel of the image. You can compute the blur radius of the kernel by multiplying the standard deviation by 3.
            The units of both the standard deviation and blur radius are DIPs.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionshadoweffect">IDCompositionShadowEffect</a>
