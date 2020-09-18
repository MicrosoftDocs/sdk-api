---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateSinusoidalTransitionFromVelocity
title: IUIAnimationTransitionLibrary2::CreateSinusoidalTransitionFromVelocity (uianimation.h)
description: Creates a sinusoidal scalar transition where amplitude is determined by initial velocity.
helpviewer_keywords: ["CreateSinusoidalTransitionFromVelocity","CreateSinusoidalTransitionFromVelocity method [Windows Animation]","CreateSinusoidalTransitionFromVelocity method [Windows Animation]","IUIAnimationTransitionLibrary2 interface","IUIAnimationTransitionLibrary2 interface [Windows Animation]","CreateSinusoidalTransitionFromVelocity method","IUIAnimationTransitionLibrary2.CreateSinusoidalTransitionFromVelocity","IUIAnimationTransitionLibrary2::CreateSinusoidalTransitionFromVelocity","uianimation.iuianimationtransitionlibrary2_createsinusoidaltransitionfromvelocity","uianimation/IUIAnimationTransitionLibrary2::CreateSinusoidalTransitionFromVelocity"]
old-location: uianimation\iuianimationtransitionlibrary2_createsinusoidaltransitionfromvelocity.htm
tech.root: UIAnimation
ms.assetid: 833D3482-68BC-45DD-9073-B048E11CB801
ms.date: 12/05/2018
ms.keywords: CreateSinusoidalTransitionFromVelocity, CreateSinusoidalTransitionFromVelocity method [Windows Animation], CreateSinusoidalTransitionFromVelocity method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateSinusoidalTransitionFromVelocity method, IUIAnimationTransitionLibrary2.CreateSinusoidalTransitionFromVelocity, IUIAnimationTransitionLibrary2::CreateSinusoidalTransitionFromVelocity, uianimation.iuianimationtransitionlibrary2_createsinusoidaltransitionfromvelocity, uianimation/IUIAnimationTransitionLibrary2::CreateSinusoidalTransitionFromVelocity
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
 - IUIAnimationTransitionLibrary2::CreateSinusoidalTransitionFromVelocity
 - uianimation/IUIAnimationTransitionLibrary2::CreateSinusoidalTransitionFromVelocity
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
 - IUIAnimationTransitionLibrary2.CreateSinusoidalTransitionFromVelocity
---

# IUIAnimationTransitionLibrary2::CreateSinusoidalTransitionFromVelocity


## -description

Creates a sinusoidal scalar transition where amplitude is determined by initial velocity.

## -parameters

### -param duration [in]

The duration of the transition.

### -param period [in]

The period of oscillation of the sinusoidal wave.

### -param transition [out]

The new sinusoidal-velocity transition.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

The value of the animation variable oscillates around the initial value over the entire duration of a sinusoidal-range transition. The amplitude of the oscillation is determined by the velocity when the transition begins.

The following figure shows the change in value over time of an animation variable during a sinusoidal-velocity transition.

<img alt="Diagram showing a sinusoidal-velocity transition" src="Images/SinusolidalTransitionFromVelocity.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary2">IUIAnimationTransitionLibrary2</a>