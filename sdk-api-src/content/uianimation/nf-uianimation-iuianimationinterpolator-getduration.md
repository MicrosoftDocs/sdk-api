---
UID: NF:uianimation.IUIAnimationInterpolator.GetDuration
title: IUIAnimationInterpolator::GetDuration (uianimation.h)
description: Gets the duration of a transition.
helpviewer_keywords: ["GetDuration","GetDuration method [Windows Animation]","GetDuration method [Windows Animation]","IUIAnimationInterpolator interface","IUIAnimationInterpolator interface [Windows Animation]","GetDuration method","IUIAnimationInterpolator.GetDuration","IUIAnimationInterpolator::GetDuration","uianimation.iuianimationinterpolator_getduration","uianimation/IUIAnimationInterpolator::GetDuration"]
old-location: uianimation\iuianimationinterpolator_getduration.htm
tech.root: UIAnimation
ms.assetid: c39acf72-7c03-4d8b-b4f2-776e4b32f781
ms.date: 12/05/2018
ms.keywords: GetDuration, GetDuration method [Windows Animation], GetDuration method [Windows Animation],IUIAnimationInterpolator interface, IUIAnimationInterpolator interface [Windows Animation],GetDuration method, IUIAnimationInterpolator.GetDuration, IUIAnimationInterpolator::GetDuration, uianimation.iuianimationinterpolator_getduration, uianimation/IUIAnimationInterpolator::GetDuration
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps \| UWP apps]
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
 - IUIAnimationInterpolator::GetDuration
 - uianimation/IUIAnimationInterpolator::GetDuration
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
 - IUIAnimationInterpolator.GetDuration
---

# IUIAnimationInterpolator::GetDuration


## -description

Gets the duration of a transition.

## -parameters

### -param duration [out]

The duration of the transition.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Windows Animation always calls the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationinterpolator-setinitialvalueandvelocity">SetInitialValueAndVelocity</a> method to set the initial value and velocity before calling <b>GetDuration</b>, so a custom interpolator need not check whether the initial value and velocity have been set.

Windows Animation can call <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationinterpolator-setinitialvalueandvelocity">SetInitialValueAndVelocity</a> multiple times with different parameters. Interpolators can cache internal state to improve performance, but they must update this cached state each time <b>SetInitialValueAndVelocity</b> is called and ensure that the results of subsequent calls to <b>GetDuration</b> reflect the updated state.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator">IUIAnimationInterpolator</a>



<a href="/windows/desktop/UIAnimation/ui-animation-seconds">UI_ANIMATION_SECONDS</a>