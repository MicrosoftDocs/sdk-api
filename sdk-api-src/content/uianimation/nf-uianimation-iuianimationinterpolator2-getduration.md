---
UID: NF:uianimation.IUIAnimationInterpolator2.GetDuration
title: IUIAnimationInterpolator2::GetDuration (uianimation.h)
description: Gets the duration of a transition for the given dimension.
helpviewer_keywords: ["GetDuration","GetDuration method [Windows Animation]","GetDuration method [Windows Animation]","IUIAnimationInterpolator2 interface","IUIAnimationInterpolator2 interface [Windows Animation]","GetDuration method","IUIAnimationInterpolator2.GetDuration","IUIAnimationInterpolator2::GetDuration","uianimation.iuianimationinterpolator2_getduration","uianimation/IUIAnimationInterpolator2::GetDuration"]
old-location: uianimation\iuianimationinterpolator2_getduration.htm
tech.root: UIAnimation
ms.assetid: 962FAF0A-CFA9-4F0D-AADC-75B42E788151
ms.date: 12/05/2018
ms.keywords: GetDuration, GetDuration method [Windows Animation], GetDuration method [Windows Animation],IUIAnimationInterpolator2 interface, IUIAnimationInterpolator2 interface [Windows Animation],GetDuration method, IUIAnimationInterpolator2.GetDuration, IUIAnimationInterpolator2::GetDuration, uianimation.iuianimationinterpolator2_getduration, uianimation/IUIAnimationInterpolator2::GetDuration
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAnimation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAnimationInterpolator2::GetDuration
 - uianimation/IUIAnimationInterpolator2::GetDuration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationInterpolator2.GetDuration
---

# IUIAnimationInterpolator2::GetDuration


## -description

Gets the duration of a transition for the given dimension.

## -parameters

### -param duration [out]

The duration of the transition.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Windows Animation always calls the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationinterpolator2-setinitialvalueandvelocity">IUIAnimationInterpolator2::SetInitialValueAndVelocity</a> method to set the initial value and velocity before calling <b>GetDuration</b>, so a custom interpolator need not check whether the initial value and velocity have been set.

Windows Animation can call <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationinterpolator2-setinitialvalueandvelocity">SetInitialValueAndVelocity</a> multiple times with different parameters. Interpolators can cache internal state to improve performance, but they must update this cached state each time <b>SetInitialValueAndVelocity</b> is called and ensure that the results of subsequent calls to <b>GetDuration</b> reflect the updated state.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator2">IUIAnimationInterpolator2</a>