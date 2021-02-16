---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateParabolicTransitionFromAcceleration
title: IUIAnimationTransitionLibrary2::CreateParabolicTransitionFromAcceleration (uianimation.h)
description: Creates a parabolic-acceleration scalar transition.
helpviewer_keywords: ["CreateParabolicTransitionFromAcceleration","CreateParabolicTransitionFromAcceleration method [Windows Animation]","CreateParabolicTransitionFromAcceleration method [Windows Animation]","IUIAnimationTransitionLibrary2 interface","IUIAnimationTransitionLibrary2 interface [Windows Animation]","CreateParabolicTransitionFromAcceleration method","IUIAnimationTransitionLibrary2.CreateParabolicTransitionFromAcceleration","IUIAnimationTransitionLibrary2::CreateParabolicTransitionFromAcceleration","uianimation.iuianimationtransitionlibrary2_createparabolictransitionfromacceleration","uianimation/IUIAnimationTransitionLibrary2::CreateParabolicTransitionFromAcceleration"]
old-location: uianimation\iuianimationtransitionlibrary2_createparabolictransitionfromacceleration.htm
tech.root: UIAnimation
ms.assetid: C2005144-CA40-4835-8AFA-7E87AE99867F
ms.date: 12/05/2018
ms.keywords: CreateParabolicTransitionFromAcceleration, CreateParabolicTransitionFromAcceleration method [Windows Animation], CreateParabolicTransitionFromAcceleration method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateParabolicTransitionFromAcceleration method, IUIAnimationTransitionLibrary2.CreateParabolicTransitionFromAcceleration, IUIAnimationTransitionLibrary2::CreateParabolicTransitionFromAcceleration, uianimation.iuianimationtransitionlibrary2_createparabolictransitionfromacceleration, uianimation/IUIAnimationTransitionLibrary2::CreateParabolicTransitionFromAcceleration
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
 - IUIAnimationTransitionLibrary2::CreateParabolicTransitionFromAcceleration
 - uianimation/IUIAnimationTransitionLibrary2::CreateParabolicTransitionFromAcceleration
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
 - IUIAnimationTransitionLibrary2.CreateParabolicTransitionFromAcceleration
---

# IUIAnimationTransitionLibrary2::CreateParabolicTransitionFromAcceleration


## -description

Creates a parabolic-acceleration scalar transition.

## -parameters

### -param finalValue [in]

The value of the animation variable at the end of the transition.

### -param finalVelocity [in]

The velocity, in units/second, at the end of the transition.

### -param acceleration [in]

The acceleration, in units/second², during the transition.

### -param transition [out]

The new parabolic-acceleration transition.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

During a parabolic-acceleration transition, the value of the animation variable changes from the  initial value to the final value, ending at the specified velocity.  You can control how quickly the variable reaches the final value by specifying the rate of acceleration.

The following figure shows the change in value over time of an animation variable during a parabolic-acceleration transition.

<img alt="Diagram showing a parabolic-acceleration transition" src="Images/ParabolicTransitionFromAcceleration.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary2">IUIAnimationTransitionLibrary2</a>