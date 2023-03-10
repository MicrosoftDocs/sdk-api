---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateDiscreteTransition
title: IUIAnimationTransitionLibrary::CreateDiscreteTransition (uianimation.h)
description: Creates a discrete transition.
helpviewer_keywords: ["CreateDiscreteTransition","CreateDiscreteTransition method [Windows Animation]","CreateDiscreteTransition method [Windows Animation]","IUIAnimationTransitionLibrary interface","IUIAnimationTransitionLibrary interface [Windows Animation]","CreateDiscreteTransition method","IUIAnimationTransitionLibrary.CreateDiscreteTransition","IUIAnimationTransitionLibrary::CreateDiscreteTransition","uianimation.iuianimationtransitionlibrary_creatediscretetransition","uianimation/IUIAnimationTransitionLibrary::CreateDiscreteTransition"]
old-location: uianimation\iuianimationtransitionlibrary_creatediscretetransition.htm
tech.root: UIAnimation
ms.assetid: 7c3f6ccb-7a42-4a48-90ad-dba99c67aa6f
ms.date: 12/05/2018
ms.keywords: CreateDiscreteTransition, CreateDiscreteTransition method [Windows Animation], CreateDiscreteTransition method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateDiscreteTransition method, IUIAnimationTransitionLibrary.CreateDiscreteTransition, IUIAnimationTransitionLibrary::CreateDiscreteTransition, uianimation.iuianimationtransitionlibrary_creatediscretetransition, uianimation/IUIAnimationTransitionLibrary::CreateDiscreteTransition
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
 - IUIAnimationTransitionLibrary::CreateDiscreteTransition
 - uianimation/IUIAnimationTransitionLibrary::CreateDiscreteTransition
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
 - IUIAnimationTransitionLibrary.CreateDiscreteTransition
---

# IUIAnimationTransitionLibrary::CreateDiscreteTransition


## -description

Creates a discrete transition.

## -parameters

### -param delay [in]

The amount of time by which to delay the instantaneous switch to the final value.

### -param finalValue [in]

The value of the animation variable at the end of the transition.

### -param hold [in]

The amount of time by which to hold the variable at its final value.

### -param transition [out]

The new discrete transition.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

During a discrete transition, the animation variable remains at the initial value for a specified delay time, then switches instantaneously to a specified final value and remains at that value for a given hold time.

The figure below shows the effect on an animation variable over time during a discrete transition.

<img alt="Diagram showing a discrete transition" src="Images/DiscreteTransition.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary">IUIAnimationTransitionLibrary</a>