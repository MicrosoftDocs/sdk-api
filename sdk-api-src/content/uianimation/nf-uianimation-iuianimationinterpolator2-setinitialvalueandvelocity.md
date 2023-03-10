---
UID: NF:uianimation.IUIAnimationInterpolator2.SetInitialValueAndVelocity
title: IUIAnimationInterpolator2::SetInitialValueAndVelocity (uianimation.h)
description: Sets the initial value and velocity of the transition for the given dimension.
helpviewer_keywords: ["IUIAnimationInterpolator2 interface [Windows Animation]","SetInitialValueAndVelocity method","IUIAnimationInterpolator2.SetInitialValueAndVelocity","IUIAnimationInterpolator2::SetInitialValueAndVelocity","SetInitialValueAndVelocity","SetInitialValueAndVelocity method [Windows Animation]","SetInitialValueAndVelocity method [Windows Animation]","IUIAnimationInterpolator2 interface","uianimation.iuianimationinterpolator2_setinitialvalueandvelocity","uianimation/IUIAnimationInterpolator2::SetInitialValueAndVelocity"]
old-location: uianimation\iuianimationinterpolator2_setinitialvalueandvelocity.htm
tech.root: UIAnimation
ms.assetid: F1C0C54D-86C3-4B65-96A4-66D89F2B2084
ms.date: 12/05/2018
ms.keywords: IUIAnimationInterpolator2 interface [Windows Animation],SetInitialValueAndVelocity method, IUIAnimationInterpolator2.SetInitialValueAndVelocity, IUIAnimationInterpolator2::SetInitialValueAndVelocity, SetInitialValueAndVelocity, SetInitialValueAndVelocity method [Windows Animation], SetInitialValueAndVelocity method [Windows Animation],IUIAnimationInterpolator2 interface, uianimation.iuianimationinterpolator2_setinitialvalueandvelocity, uianimation/IUIAnimationInterpolator2::SetInitialValueAndVelocity
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
 - IUIAnimationInterpolator2::SetInitialValueAndVelocity
 - uianimation/IUIAnimationInterpolator2::SetInitialValueAndVelocity
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
 - IUIAnimationInterpolator2.SetInitialValueAndVelocity
---

# IUIAnimationInterpolator2::SetInitialValueAndVelocity


## -description

Sets the initial value and velocity of the transition for the given dimension.

## -parameters

### -param initialValue [in]

The initial value.

### -param initialVelocity [in]

The initial velocity.

### -param cDimension [in]

The dimension in which to set the initial value or velocity of the transition.

## -returns

Returns <b>S_OK</b> if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Windows Animation always calls <b>SetInitialValueAndVelocity</b> before calling the other methods of  <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator2">IUIAnimationInterpolator2</a> at different offsets. However, <b>SetInitialValueAndVelocity</b> can be called multiple times with different parameters. Interpolators can cache internal state to improve performance, but they must update this cached state each time <b>SetInitialValueAndVelocity</b> is called and ensure that the results of subsequent calls to these methods reflect the updated state.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator2">IUIAnimationInterpolator2</a>