---
UID: NF:uianimation.IUIAnimationInterpolator2.SetDuration
title: IUIAnimationInterpolator2::SetDuration (uianimation.h)
description: Sets the duration of the transition in the given dimension.
helpviewer_keywords: ["IUIAnimationInterpolator2 interface [Windows Animation]","SetDuration method","IUIAnimationInterpolator2.SetDuration","IUIAnimationInterpolator2::SetDuration","SetDuration","SetDuration method [Windows Animation]","SetDuration method [Windows Animation]","IUIAnimationInterpolator2 interface","uianimation.iuianimationinterpolator2_setduration","uianimation/IUIAnimationInterpolator2::SetDuration"]
old-location: uianimation\iuianimationinterpolator2_setduration.htm
tech.root: UIAnimation
ms.assetid: C1E6EC87-283A-4C56-96C5-531C5C5F5575
ms.date: 12/05/2018
ms.keywords: IUIAnimationInterpolator2 interface [Windows Animation],SetDuration method, IUIAnimationInterpolator2.SetDuration, IUIAnimationInterpolator2::SetDuration, SetDuration, SetDuration method [Windows Animation], SetDuration method [Windows Animation],IUIAnimationInterpolator2 interface, uianimation.iuianimationinterpolator2_setduration, uianimation/IUIAnimationInterpolator2::SetDuration
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
 - IUIAnimationInterpolator2::SetDuration
 - uianimation/IUIAnimationInterpolator2::SetDuration
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
 - IUIAnimationInterpolator2.SetDuration
---

# IUIAnimationInterpolator2::SetDuration


## -description

Sets the duration of the transition in the given dimension.

## -parameters

### -param duration [in, out]

The duration of the transition.

## -returns

Returns <b>S_OK</b> if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Windows Animation calls this method only after calling the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationinterpolator2-getdependencies">IUIAnimationInterpolator2::GetDependencies</a> method, and only if that call returns <b>UI_ANIMATION_DEPENDENCY_DURATION</b> as one of its <i>durationDependencies</i> flags.

Typically, an interpolator with a duration dependency has a duration parameter in the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionfactory">IUIAnimationTransitionFactory</a> or <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionfactory2">IUIAnimationTransitionFactory2</a> creation method  that is associated with that interpolator.  The interpolator should store its duration when first initialized and overwrite the duration when <b>SetDuration</b> is called.

Windows Animation always calls the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationinterpolator2-setinitialvalueandvelocity">IUIAnimationInterpolator2::SetInitialValueAndVelocity</a> method to set the initial value and velocity before calling <b>SetDuration</b>, so a custom interpolator doesn't need to check whether the initial value and velocity have been set.

Windows Animation can call <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationinterpolator2-setinitialvalueandvelocity">SetInitialValueAndVelocity</a> and <b>SetDuration</b> multiple times with different parameters. Interpolators can cache internal state to improve performance, but they must update this cached state each time <b>SetInitialValueAndVelocity</b> is called and ensure that the results of subsequent calls to <b>SetDuration</b> reflect the updated state.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator2">IUIAnimationInterpolator2</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_dependencies">UI_ANIMATION_DEPENDENCIES</a>



<a href="/windows/desktop/UIAnimation/ui-animation-seconds">UI_ANIMATION_SECONDS</a>