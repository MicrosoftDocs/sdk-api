---
UID: NF:uianimation.IUIAnimationInterpolator2.InterpolateValue
title: IUIAnimationInterpolator2::InterpolateValue (uianimation.h)
description: Interpolates the value of an animation variable at the specified offset and for the given dimension.
helpviewer_keywords: ["IUIAnimationInterpolator2 interface [Windows Animation]","InterpolateValue method","IUIAnimationInterpolator2.InterpolateValue","IUIAnimationInterpolator2::InterpolateValue","InterpolateValue","InterpolateValue method [Windows Animation]","InterpolateValue method [Windows Animation]","IUIAnimationInterpolator2 interface","uianimation.iuianimationinterpolator2_interpolatevalue","uianimation/IUIAnimationInterpolator2::InterpolateValue"]
old-location: uianimation\iuianimationinterpolator2_interpolatevalue.htm
tech.root: UIAnimation
ms.assetid: A512B264-642A-4E4B-9AEA-DE80B9D99A53
ms.date: 12/05/2018
ms.keywords: IUIAnimationInterpolator2 interface [Windows Animation],InterpolateValue method, IUIAnimationInterpolator2.InterpolateValue, IUIAnimationInterpolator2::InterpolateValue, InterpolateValue, InterpolateValue method [Windows Animation], InterpolateValue method [Windows Animation],IUIAnimationInterpolator2 interface, uianimation.iuianimationinterpolator2_interpolatevalue, uianimation/IUIAnimationInterpolator2::InterpolateValue
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
 - IUIAnimationInterpolator2::InterpolateValue
 - uianimation/IUIAnimationInterpolator2::InterpolateValue
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
 - IUIAnimationInterpolator2.InterpolateValue
---

# IUIAnimationInterpolator2::InterpolateValue


## -description

Interpolates the value of an animation variable at the specified offset and for the given dimension.

## -parameters

### -param offset [in]

The offset from the start of the transition.

This parameter is always greater than or equal to zero and less than the duration of the transition. This method is not called if the duration of the transition is zero.

### -param value [out]

The interpolated value.

### -param cDimension [in]

The dimension in which to interpolate the value.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Windows Animation always calls the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationinterpolator2-setinitialvalueandvelocity">IUIAnimationInterpolator2::SetInitialValueAndVelocity</a> method to set the initial value and velocity before calling <b>InterpolateValue</b>, so a custom interpolator need not check whether the initial value and velocity have been set.

Windows Animation can call <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationinterpolator2-setinitialvalueandvelocity">SetInitialValueAndVelocity</a> multiple times with different parameters. Interpolators can cache internal state to improve performance, but they must update this cached state each time <b>SetInitialValueAndVelocity</b> is called and ensure that the results of subsequent calls to <b>InterpolateValue</b> reflect the updated state.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator2">IUIAnimationInterpolator2</a>



<a href="/windows/desktop/UIAnimation/ui-animation-seconds">UI_ANIMATION_SECONDS</a>