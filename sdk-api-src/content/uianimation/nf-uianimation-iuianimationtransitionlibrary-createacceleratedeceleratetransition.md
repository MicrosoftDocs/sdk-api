---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateAccelerateDecelerateTransition
title: IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition (uianimation.h)
description: Creates an accelerate-decelerate transition.
helpviewer_keywords: ["CreateAccelerateDecelerateTransition","CreateAccelerateDecelerateTransition method [Windows Animation]","CreateAccelerateDecelerateTransition method [Windows Animation]","IUIAnimationTransitionLibrary interface","IUIAnimationTransitionLibrary interface [Windows Animation]","CreateAccelerateDecelerateTransition method","IUIAnimationTransitionLibrary.CreateAccelerateDecelerateTransition","IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition","uianimation.iuianimationtransitionlibrary_createacceleratedeceleratetransition","uianimation/IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition"]
old-location: uianimation\iuianimationtransitionlibrary_createacceleratedeceleratetransition.htm
tech.root: UIAnimation
ms.assetid: 97a0c6cc-991b-464f-b000-1d1199c5f4de
ms.date: 12/05/2018
ms.keywords: CreateAccelerateDecelerateTransition, CreateAccelerateDecelerateTransition method [Windows Animation], CreateAccelerateDecelerateTransition method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateAccelerateDecelerateTransition method, IUIAnimationTransitionLibrary.CreateAccelerateDecelerateTransition, IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition, uianimation.iuianimationtransitionlibrary_createacceleratedeceleratetransition, uianimation/IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition
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
 - IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition
 - uianimation/IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition
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
 - IUIAnimationTransitionLibrary.CreateAccelerateDecelerateTransition
---

# IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition


## -description

Creates an accelerate-decelerate transition.

## -parameters

### -param duration [in]

The duration of the transition.

### -param finalValue [in]

The value of the animation variable at the end of the transition.

### -param accelerationRatio [in]

The ratio of the time spent accelerating to the duration.

### -param decelerationRatio [in]

The ratio of the time spent decelerating to the duration.

### -param transition [out]

The new accelerate-decelerate transition.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

During an accelerate-decelerate transition, the animation variable
      speeds up and then slows down over the duration of the transition, ending at a specified value. You can control how quickly the variable accelerates and decelerates independently, by specifying different acceleration and deceleration ratios.

When the initial velocity is zero, the acceleration ratio is the fraction of the duration that the variable will spend accelerating; likewise with the deceleration ratio. If the initial velocity is nonzero, it is the fraction of the time between the velocity reaching zero and the end of transition. The acceleration ratio and the deceleration ratio should sum to a maximum of 1.0. 

The figures below show the effect on animation variables with different initial velocities during accelerate-decelerate transitions.

<img alt="Diagram showing accelerate-decelerate transitions" src="Images/AccelerateDecelerateTransition.png"/>
<div class="alert"><b>Note</b>  d' in the above figure on the right shows the time between the velocity reaching zero and the end of the transition.</div>
<div> </div>

#### Examples

For an example, see <a href="/windows/desktop/UIAnimation/updating---timer-driven-animation">Create a Storyboard and Add Transitions</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary">IUIAnimationTransitionLibrary</a>