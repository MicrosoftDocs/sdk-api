---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateCubicTransition
title: IUIAnimationTransitionLibrary2::CreateCubicTransition (uianimation.h)
description: Creates a cubic scalar transition.
helpviewer_keywords: ["CreateCubicTransition","CreateCubicTransition method [Windows Animation]","CreateCubicTransition method [Windows Animation]","IUIAnimationTransitionLibrary2 interface","IUIAnimationTransitionLibrary2 interface [Windows Animation]","CreateCubicTransition method","IUIAnimationTransitionLibrary2.CreateCubicTransition","IUIAnimationTransitionLibrary2::CreateCubicTransition","uianimation.iuianimationtransitionlibrary2_createcubictransition","uianimation/IUIAnimationTransitionLibrary2::CreateCubicTransition"]
old-location: uianimation\iuianimationtransitionlibrary2_createcubictransition.htm
tech.root: UIAnimation
ms.assetid: 63ADBD53-2552-4D68-AABD-E3B1F83831EB
ms.date: 12/05/2018
ms.keywords: CreateCubicTransition, CreateCubicTransition method [Windows Animation], CreateCubicTransition method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateCubicTransition method, IUIAnimationTransitionLibrary2.CreateCubicTransition, IUIAnimationTransitionLibrary2::CreateCubicTransition, uianimation.iuianimationtransitionlibrary2_createcubictransition, uianimation/IUIAnimationTransitionLibrary2::CreateCubicTransition
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
 - IUIAnimationTransitionLibrary2::CreateCubicTransition
 - uianimation/IUIAnimationTransitionLibrary2::CreateCubicTransition
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
 - IUIAnimationTransitionLibrary2.CreateCubicTransition
---

# IUIAnimationTransitionLibrary2::CreateCubicTransition


## -description

Creates a cubic scalar transition.

## -parameters

### -param duration [in]

The duration of the transition.

### -param finalValue [in]

The value of the animation variable at the end of the transition.

### -param finalVelocity [in]

The velocity of the variable at the end of the transition.

### -param transition [out]

The new cubic transition.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

During a cubic transition, the value of the animation variable changes from its initial value to the <i>finalValue</i> over the <i>duration</i> of the transition, ending at the <i>finalVelocity</i>.

The following figure shows the effect on an animation variable over time during a cubic transition.

<img alt="Diagram showing a cubic transition" src="Images/CubicTransition.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary2">IUIAnimationTransitionLibrary2</a>