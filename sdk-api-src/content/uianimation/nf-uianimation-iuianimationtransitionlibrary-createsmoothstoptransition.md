---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateSmoothStopTransition
title: IUIAnimationTransitionLibrary::CreateSmoothStopTransition (uianimation.h)
description: Creates a smooth-stop transition.
helpviewer_keywords: ["CreateSmoothStopTransition","CreateSmoothStopTransition method [Windows Animation]","CreateSmoothStopTransition method [Windows Animation]","IUIAnimationTransitionLibrary interface","IUIAnimationTransitionLibrary interface [Windows Animation]","CreateSmoothStopTransition method","IUIAnimationTransitionLibrary.CreateSmoothStopTransition","IUIAnimationTransitionLibrary::CreateSmoothStopTransition","uianimation.iuianimationtransitionlibrary_createsmoothstoptransition","uianimation/IUIAnimationTransitionLibrary::CreateSmoothStopTransition"]
old-location: uianimation\iuianimationtransitionlibrary_createsmoothstoptransition.htm
tech.root: UIAnimation
ms.assetid: fce15425-5529-4ebf-9961-7e125cc64edb
ms.date: 12/05/2018
ms.keywords: CreateSmoothStopTransition, CreateSmoothStopTransition method [Windows Animation], CreateSmoothStopTransition method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateSmoothStopTransition method, IUIAnimationTransitionLibrary.CreateSmoothStopTransition, IUIAnimationTransitionLibrary::CreateSmoothStopTransition, uianimation.iuianimationtransitionlibrary_createsmoothstoptransition, uianimation/IUIAnimationTransitionLibrary::CreateSmoothStopTransition
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
 - IUIAnimationTransitionLibrary::CreateSmoothStopTransition
 - uianimation/IUIAnimationTransitionLibrary::CreateSmoothStopTransition
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
 - IUIAnimationTransitionLibrary.CreateSmoothStopTransition
---

# IUIAnimationTransitionLibrary::CreateSmoothStopTransition


## -description

Creates a smooth-stop transition.

## -parameters

### -param maximumDuration [in]

The maximum duration of the transition.

### -param finalValue [in]

The value of the animation variable at the end of the transition.

### -param transition [out]

The new smooth-stop transition.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

A smooth-stop transition slows down as it approaches the specified final value, and reaches it with a velocity of zero. The duration of the transition is determined by the initial velocity, the difference between the initial and final values, and the specified maximum duration. If there is no solution consisting of a single parabolic arc, this method creates a cubic transition.

The figure below shows the effect on an animation variable over time during a smooth-stop transition.

<img alt="Diagram showing a smooth stop transition" src="Images/SmoothStopTransition.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary">IUIAnimationTransitionLibrary</a>