---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateSinusoidalTransitionFromVelocity
title: IUIAnimationTransitionLibrary::CreateSinusoidalTransitionFromVelocity (uianimation.h)
description: Creates a sinusoidal-velocity transition, with an amplitude determined by the initial velocity.
helpviewer_keywords: ["CreateSinusoidalTransitionFromVelocity","CreateSinusoidalTransitionFromVelocity method [Windows Animation]","CreateSinusoidalTransitionFromVelocity method [Windows Animation]","IUIAnimationTransitionLibrary interface","IUIAnimationTransitionLibrary interface [Windows Animation]","CreateSinusoidalTransitionFromVelocity method","IUIAnimationTransitionLibrary.CreateSinusoidalTransitionFromVelocity","IUIAnimationTransitionLibrary::CreateSinusoidalTransitionFromVelocity","uianimation.iuianimationtransitionlibrary_createsinusoidaltransitionfromvelocity","uianimation/IUIAnimationTransitionLibrary::CreateSinusoidalTransitionFromVelocity"]
old-location: uianimation\iuianimationtransitionlibrary_createsinusoidaltransitionfromvelocity.htm
tech.root: UIAnimation
ms.assetid: 47998787-dcd5-4973-bf7e-30096b01c51b
ms.date: 12/05/2018
ms.keywords: CreateSinusoidalTransitionFromVelocity, CreateSinusoidalTransitionFromVelocity method [Windows Animation], CreateSinusoidalTransitionFromVelocity method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateSinusoidalTransitionFromVelocity method, IUIAnimationTransitionLibrary.CreateSinusoidalTransitionFromVelocity, IUIAnimationTransitionLibrary::CreateSinusoidalTransitionFromVelocity, uianimation.iuianimationtransitionlibrary_createsinusoidaltransitionfromvelocity, uianimation/IUIAnimationTransitionLibrary::CreateSinusoidalTransitionFromVelocity
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
 - IUIAnimationTransitionLibrary::CreateSinusoidalTransitionFromVelocity
 - uianimation/IUIAnimationTransitionLibrary::CreateSinusoidalTransitionFromVelocity
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
 - IUIAnimationTransitionLibrary.CreateSinusoidalTransitionFromVelocity
---

# IUIAnimationTransitionLibrary::CreateSinusoidalTransitionFromVelocity


## -description

Creates a sinusoidal-velocity transition, with an amplitude determined by the initial velocity.

## -parameters

### -param duration [in]

The duration of the transition.

### -param period [in]

The period of oscillation of the sinusoidal wave in seconds.

### -param transition [out]

The new sinusoidal-velocity transition.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

The value of the animation variable oscillates around the initial value over the entire duration of a sinusoidal-range transition. The amplitude of the oscillation is determined by the velocity when the transition begins.

The figure below shows the effect on an animation variable over time during a sinusoidal-velocity transition.

<img alt="Diagram showing a sinusoidal-velocity transition" src="Images/SinusolidalTransitionFromVelocity.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary">IUIAnimationTransitionLibrary</a>