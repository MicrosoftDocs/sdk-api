---
UID: NF:uianimation.IUIAnimationInterpolator.SetInitialValueAndVelocity
title: IUIAnimationInterpolator::SetInitialValueAndVelocity (uianimation.h)
description: Sets the initial value and velocity at the start of the transition.
helpviewer_keywords: ["IUIAnimationInterpolator interface [Windows Animation]","SetInitialValueAndVelocity method","IUIAnimationInterpolator.SetInitialValueAndVelocity","IUIAnimationInterpolator::SetInitialValueAndVelocity","SetInitialValueAndVelocity","SetInitialValueAndVelocity method [Windows Animation]","SetInitialValueAndVelocity method [Windows Animation]","IUIAnimationInterpolator interface","uianimation.iuianimationinterpolator_setinitialvalueandvelocity","uianimation/IUIAnimationInterpolator::SetInitialValueAndVelocity"]
old-location: uianimation\iuianimationinterpolator_setinitialvalueandvelocity.htm
tech.root: UIAnimation
ms.assetid: a1c5451a-b8d0-4eb7-883c-6bd1d585cb11
ms.date: 12/05/2018
ms.keywords: IUIAnimationInterpolator interface [Windows Animation],SetInitialValueAndVelocity method, IUIAnimationInterpolator.SetInitialValueAndVelocity, IUIAnimationInterpolator::SetInitialValueAndVelocity, SetInitialValueAndVelocity, SetInitialValueAndVelocity method [Windows Animation], SetInitialValueAndVelocity method [Windows Animation],IUIAnimationInterpolator interface, uianimation.iuianimationinterpolator_setinitialvalueandvelocity, uianimation/IUIAnimationInterpolator::SetInitialValueAndVelocity
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
 - IUIAnimationInterpolator::SetInitialValueAndVelocity
 - uianimation/IUIAnimationInterpolator::SetInitialValueAndVelocity
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
 - IUIAnimationInterpolator.SetInitialValueAndVelocity
---

# IUIAnimationInterpolator::SetInitialValueAndVelocity


## -description

Sets the initial value and velocity at the start of the transition.

## -parameters

### -param initialValue [in]

The initial value.

### -param initialVelocity [in]

The initial velocity.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. 
            
See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Windows Animation always calls <b>SetInitialValueAndVelocity</b> before calling the other methods of  <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator">IUIAnimationInterpolator</a> at different offsets. However, it can be called multiple times with different parameters. Interpolators can cache internal state to improve performance, but they must update this cached state each time <b>SetInitialValueAndVelocity</b> is called and ensure that the results of subsequent calls to these methods reflect the updated state.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator">IUIAnimationInterpolator</a>