---
UID: NF:dcomp.IDCompositionGaussianBlurEffect.SetStandardDeviation(IDCompositionAnimation)
title: IDCompositionGaussianBlurEffect::SetStandardDeviation(IDCompositionAnimation) (dcomp.h)
description: The IDCompositionGaussianBlurEffect::SetStandardDeviation(IDCompositionAnimation) method sets the amount of blur to be applied to the image.
helpviewer_keywords: ["IDCompositionGaussianBlurEffect interface [DirectComposition]","SetStandardDeviation method","IDCompositionGaussianBlurEffect.SetStandardDeviation","IDCompositionGaussianBlurEffect.SetStandardDeviation(IDCompositionAnimation)","IDCompositionGaussianBlurEffect::SetStandardDeviation","IDCompositionGaussianBlurEffect::SetStandardDeviation(IDCompositionAnimation)","SetStandardDeviation","SetStandardDeviation method [DirectComposition]","SetStandardDeviation method [DirectComposition]","IDCompositionGaussianBlurEffect interface","dcomp/IDCompositionGaussianBlurEffect::SetStandardDeviation","directcomp.idcompositiongaussianblureffect_setstandarddeviation_2"]
old-location: directcomp\idcompositiongaussianblureffect_setstandarddeviation_2.htm
tech.root: directcomp
ms.assetid: EBDB097C-4B79-4E38-A09E-48FAFE6E5553
ms.date: 06/23/2022
ms.keywords: IDCompositionGaussianBlurEffect interface [DirectComposition],SetStandardDeviation method, IDCompositionGaussianBlurEffect.SetStandardDeviation, IDCompositionGaussianBlurEffect.SetStandardDeviation(IDCompositionAnimation), IDCompositionGaussianBlurEffect::SetStandardDeviation, IDCompositionGaussianBlurEffect::SetStandardDeviation(IDCompositionAnimation), SetStandardDeviation, SetStandardDeviation method [DirectComposition], SetStandardDeviation method [DirectComposition],IDCompositionGaussianBlurEffect interface, dcomp/IDCompositionGaussianBlurEffect::SetStandardDeviation, directcomp.idcompositiongaussianblureffect_setstandarddeviation_2
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
 - IDCompositionGaussianBlurEffect::SetStandardDeviation
 - dcomp/IDCompositionGaussianBlurEffect::SetStandardDeviation
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
 - IDCompositionGaussianBlurEffect.SetStandardDeviation
---

# IDCompositionGaussianBlurEffect::SetStandardDeviation(IDCompositionAnimation)


## -description

Sets the amount of blur to be applied to the image.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the amount of blur changes over time. You can compute the blur radius of the kernel by multiplying the standard deviation by 3. 
          The units of both the standard deviation and blur radius are DIPs. A value of zero DIPs disables this effect entirely. 
          This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiongaussianblureffect">IDCompositionGaussianBlurEffect</a>