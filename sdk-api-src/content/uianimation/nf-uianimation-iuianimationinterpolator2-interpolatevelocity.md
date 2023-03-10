---
UID: NF:uianimation.IUIAnimationInterpolator2.InterpolateVelocity
title: IUIAnimationInterpolator2::InterpolateVelocity (uianimation.h)
description: Interpolates the velocity, or rate of change, at the specified offset for the given dimension.
helpviewer_keywords: ["IUIAnimationInterpolator2 interface [Windows Animation]","InterpolateVelocity method","IUIAnimationInterpolator2.InterpolateVelocity","IUIAnimationInterpolator2::InterpolateVelocity","InterpolateVelocity","InterpolateVelocity method [Windows Animation]","InterpolateVelocity method [Windows Animation]","IUIAnimationInterpolator2 interface","uianimation.iuianimationinterpolator2_interpolatevelocity","uianimation/IUIAnimationInterpolator2::InterpolateVelocity"]
old-location: uianimation\iuianimationinterpolator2_interpolatevelocity.htm
tech.root: UIAnimation
ms.assetid: B6BD1B9D-3553-4A83-BB57-629611F9CA18
ms.date: 12/05/2018
ms.keywords: IUIAnimationInterpolator2 interface [Windows Animation],InterpolateVelocity method, IUIAnimationInterpolator2.InterpolateVelocity, IUIAnimationInterpolator2::InterpolateVelocity, InterpolateVelocity, InterpolateVelocity method [Windows Animation], InterpolateVelocity method [Windows Animation],IUIAnimationInterpolator2 interface, uianimation.iuianimationinterpolator2_interpolatevelocity, uianimation/IUIAnimationInterpolator2::InterpolateVelocity
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
 - IUIAnimationInterpolator2::InterpolateVelocity
 - uianimation/IUIAnimationInterpolator2::InterpolateVelocity
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
 - IUIAnimationInterpolator2.InterpolateVelocity
---

# IUIAnimationInterpolator2::InterpolateVelocity


## -description

Interpolates the velocity, or rate of change, at the specified offset for the given dimension.

## -parameters

### -param offset [in]

The offset from the start of the transition.



The offset is always greater than or equal to zero and less than or equal to the duration of the transition. This method is not called if the duration of the transition is zero.

### -param velocity [out]

The interpolated velocity.

### -param cDimension [in]

The dimension in which to interpolate the velocity.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Windows Animation always calls the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationinterpolator2-setinitialvalueandvelocity">IUIAnimationInterpolator2::SetInitialValueAndVelocity</a> method to set the initial value and velocity before calling <b>InterpolateVelocity</b>, so a custom interpolator need not check whether the initial value and velocity have been set.

Windows Animation can call <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationinterpolator2-setinitialvalueandvelocity">SetInitialValueAndVelocity</a> multiple times with different parameters. Interpolators can cache internal state to improve performance, but they must update this cached state each time <b>SetInitialValueAndVelocity</b> is called and ensure that the results of subsequent calls to <b>InterpolateVelocity</b> reflect the updated state.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator2">IUIAnimationInterpolator2</a>



<a href="/windows/desktop/UIAnimation/ui-animation-seconds">UI_ANIMATION_SECONDS</a>