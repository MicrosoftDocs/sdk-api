---
UID: NF:dcomp.IDCompositionGaussianBlurEffect.SetStandardDeviation(IDCompositionAnimation)
title: IDCompositionGaussianBlurEffect::SetStandardDeviation(IDCompositionAnimation) (dcomp.h)
author: windows-sdk-content
description: Sets the amount of blur to be applied to the image.
old-location: directcomp\idcompositiongaussianblureffect_setstandarddeviation_2.htm
tech.root: directcomp
ms.assetid: EBDB097C-4B79-4E38-A09E-48FAFE6E5553
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionGaussianBlurEffect interface [DirectComposition],SetStandardDeviation method, IDCompositionGaussianBlurEffect.SetStandardDeviation, IDCompositionGaussianBlurEffect.SetStandardDeviation(IDCompositionAnimation), IDCompositionGaussianBlurEffect::SetStandardDeviation, IDCompositionGaussianBlurEffect::SetStandardDeviation(IDCompositionAnimation), SetStandardDeviation, SetStandardDeviation method [DirectComposition], SetStandardDeviation method [DirectComposition],IDCompositionGaussianBlurEffect interface, dcomp/IDCompositionGaussianBlurEffect::SetStandardDeviation, directcomp.idcompositiongaussianblureffect_setstandarddeviation_2
ms.topic: method
f1_keywords: 
 - "dcomp/IDCompositionGaussianBlurEffect.SetStandardDeviation"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionGaussianBlurEffect.SetStandardDeviation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionGaussianBlurEffect::SetStandardDeviation(IDCompositionAnimation)


## -description


Sets the amount of blur to be applied to the image.


## -parameters




### -param animation [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the amount of blur changes over time. You can compute the blur radius of the kernel by multiplying the standard deviation by 3. 
          The units of both the standard deviation and blur radius are DIPs. A value of zero DIPs disables this effect entirely. 
          This parameter must not be NULL.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiongaussianblureffect">IDCompositionGaussianBlurEffect</a>
 

 

