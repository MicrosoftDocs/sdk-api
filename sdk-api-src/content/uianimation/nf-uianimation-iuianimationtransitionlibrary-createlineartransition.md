---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateLinearTransition
title: IUIAnimationTransitionLibrary::CreateLinearTransition (uianimation.h)
description: Creates a linear transition.
helpviewer_keywords: ["CreateLinearTransition","CreateLinearTransition method [Windows Animation]","CreateLinearTransition method [Windows Animation]","IUIAnimationTransitionLibrary interface","IUIAnimationTransitionLibrary interface [Windows Animation]","CreateLinearTransition method","IUIAnimationTransitionLibrary.CreateLinearTransition","IUIAnimationTransitionLibrary::CreateLinearTransition","uianimation.iuianimationtransitionlibrary_createlineartransition","uianimation/IUIAnimationTransitionLibrary::CreateLinearTransition"]
old-location: uianimation\iuianimationtransitionlibrary_createlineartransition.htm
tech.root: UIAnimation
ms.assetid: 51c54bc9-771c-484e-a24f-22ba03c70709
ms.date: 12/05/2018
ms.keywords: CreateLinearTransition, CreateLinearTransition method [Windows Animation], CreateLinearTransition method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateLinearTransition method, IUIAnimationTransitionLibrary.CreateLinearTransition, IUIAnimationTransitionLibrary::CreateLinearTransition, uianimation.iuianimationtransitionlibrary_createlineartransition, uianimation/IUIAnimationTransitionLibrary::CreateLinearTransition
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
 - IUIAnimationTransitionLibrary::CreateLinearTransition
 - uianimation/IUIAnimationTransitionLibrary::CreateLinearTransition
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
 - IUIAnimationTransitionLibrary.CreateLinearTransition
---

# IUIAnimationTransitionLibrary::CreateLinearTransition


## -description

Creates a linear transition.

## -parameters

### -param duration [in]

The duration of the transition.

### -param finalValue [in]

The value of the animation variable at the end of the transition.

### -param transition [out]

The new linear transition.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

During a linear transition, the value of the animation variable transitions linearly from its initial value to a  specified final value.

The figure below shows the effect on an animation variable over time during a linear transition.

<img alt="Diagram showing a linear transition" src="Images/LinearTransition.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary">IUIAnimationTransitionLibrary</a>