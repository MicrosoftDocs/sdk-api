---
UID: NF:uianimation.IUIAnimationInterpolator.SetDuration
title: IUIAnimationInterpolator::SetDuration (uianimation.h)
description: Sets the duration of the transition.
helpviewer_keywords: ["IUIAnimationInterpolator interface [Windows Animation]","SetDuration method","IUIAnimationInterpolator.SetDuration","IUIAnimationInterpolator::SetDuration","SetDuration","SetDuration method [Windows Animation]","SetDuration method [Windows Animation]","IUIAnimationInterpolator interface","uianimation.iuianimationinterpolator_setduration","uianimation/IUIAnimationInterpolator::SetDuration"]
old-location: uianimation\iuianimationinterpolator_setduration.htm
tech.root: UIAnimation
ms.assetid: 79038ada-ebc2-4259-862a-d81403c2f6b8
ms.date: 12/05/2018
ms.keywords: IUIAnimationInterpolator interface [Windows Animation],SetDuration method, IUIAnimationInterpolator.SetDuration, IUIAnimationInterpolator::SetDuration, SetDuration, SetDuration method [Windows Animation], SetDuration method [Windows Animation],IUIAnimationInterpolator interface, uianimation.iuianimationinterpolator_setduration, uianimation/IUIAnimationInterpolator::SetDuration
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
 - IUIAnimationInterpolator::SetDuration
 - uianimation/IUIAnimationInterpolator::SetDuration
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
 - IUIAnimationInterpolator.SetDuration
---

# IUIAnimationInterpolator::SetDuration


## -description

Sets the duration of the transition.

## -parameters

### -param duration [in]

The duration of the transition.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Windows Animation calls this method only after calling the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationinterpolator-getdependencies">GetDependencies</a> method, and only if that call returns <b>UI_ANIMATION_DEPENDENCY_DURATION</b> as one of its <i>durationDependencies</i> flags.

Typically, an interpolator with a duration dependency will have a duration parameter in its associated creation method of <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionfactory">IUIAnimationTransitionFactory</a>.  The interpolator should store its duration when first initialized and overwrite it when <b>SetDuration</b> is called.

Windows Animation always calls the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationinterpolator-setinitialvalueandvelocity">SetInitialValueAndVelocity</a> method to set the initial value and velocity before calling <b>SetDuration</b>, so a custom interpolator need not check whether the initial value and velocity have been set.

Windows Animation can call <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationinterpolator-setinitialvalueandvelocity">SetInitialValueAndVelocity</a> and <b>SetDuration</b> multiple times with different parameters. Interpolators can cache internal state to improve performance, but they must update this cached state each time <b>SetInitialValueAndVelocity</b> is called and ensure that the results of subsequent calls to <b>SetDuration</b> reflect the updated state.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator">IUIAnimationInterpolator</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_dependencies">UI_ANIMATION_DEPENDENCIES</a>



<a href="/windows/desktop/UIAnimation/ui-animation-seconds">UI_ANIMATION_SECONDS</a>