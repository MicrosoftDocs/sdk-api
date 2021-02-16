---
UID: NF:uianimation.IUIAnimationInterpolator.InterpolateVelocity
title: IUIAnimationInterpolator::InterpolateVelocity (uianimation.h)
description: Interpolates the velocity, or rate of change, at the specified offset.
helpviewer_keywords: ["IUIAnimationInterpolator interface [Windows Animation]","InterpolateVelocity method","IUIAnimationInterpolator.InterpolateVelocity","IUIAnimationInterpolator::InterpolateVelocity","InterpolateVelocity","InterpolateVelocity method [Windows Animation]","InterpolateVelocity method [Windows Animation]","IUIAnimationInterpolator interface","uianimation.iuianimationinterpolator_interpolatevelocity","uianimation/IUIAnimationInterpolator::InterpolateVelocity"]
old-location: uianimation\iuianimationinterpolator_interpolatevelocity.htm
tech.root: UIAnimation
ms.assetid: ae0b6674-307b-454e-b8be-db564c234607
ms.date: 12/05/2018
ms.keywords: IUIAnimationInterpolator interface [Windows Animation],InterpolateVelocity method, IUIAnimationInterpolator.InterpolateVelocity, IUIAnimationInterpolator::InterpolateVelocity, InterpolateVelocity, InterpolateVelocity method [Windows Animation], InterpolateVelocity method [Windows Animation],IUIAnimationInterpolator interface, uianimation.iuianimationinterpolator_interpolatevelocity, uianimation/IUIAnimationInterpolator::InterpolateVelocity
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
 - IUIAnimationInterpolator::InterpolateVelocity
 - uianimation/IUIAnimationInterpolator::InterpolateVelocity
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
 - IUIAnimationInterpolator.InterpolateVelocity
---

# IUIAnimationInterpolator::InterpolateVelocity


## -description

Interpolates the velocity, or rate of change, at the specified offset.

## -parameters

### -param offset [in]

The offset from the start of the transition.

The offset is always greater than or equal to zero and less than or equal to the duration of the transition. This method is not called if the duration of the transition is zero.

### -param velocity [out]

The interpolated velocity.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Windows Animation always calls the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationinterpolator-setinitialvalueandvelocity">SetInitialValueAndVelocity</a> method to set the initial value and velocity before calling <b>InterpolateVelocity</b>, so a custom interpolator need not check whether the initial value and velocity have been set.

Windows Animation can call <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationinterpolator-setinitialvalueandvelocity">SetInitialValueAndVelocity</a> multiple times with different parameters. Interpolators can cache internal state to improve performance, but they must update this cached state each time <b>SetInitialValueAndVelocity</b> is called and ensure that the results of subsequent calls to <b>InterpolateVelocity</b> reflect the updated state.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator">IUIAnimationInterpolator</a>



<a href="/windows/desktop/UIAnimation/ui-animation-seconds">UI_ANIMATION_SECONDS</a>