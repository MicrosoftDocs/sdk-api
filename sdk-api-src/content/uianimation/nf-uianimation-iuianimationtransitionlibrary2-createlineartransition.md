---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateLinearTransition
title: IUIAnimationTransitionLibrary2::CreateLinearTransition (uianimation.h)
description: Creates a linear scalar transition.
helpviewer_keywords: ["CreateLinearTransition","CreateLinearTransition method [Windows Animation]","CreateLinearTransition method [Windows Animation]","IUIAnimationTransitionLibrary2 interface","IUIAnimationTransitionLibrary2 interface [Windows Animation]","CreateLinearTransition method","IUIAnimationTransitionLibrary2.CreateLinearTransition","IUIAnimationTransitionLibrary2::CreateLinearTransition","uianimation.iuianimationtransitionlibrary2_createlineartransition","uianimation/IUIAnimationTransitionLibrary2::CreateLinearTransition"]
old-location: uianimation\iuianimationtransitionlibrary2_createlineartransition.htm
tech.root: UIAnimation
ms.assetid: BD0A9D4E-0306-4C76-8CC2-AA1A747C4538
ms.date: 12/05/2018
ms.keywords: CreateLinearTransition, CreateLinearTransition method [Windows Animation], CreateLinearTransition method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateLinearTransition method, IUIAnimationTransitionLibrary2.CreateLinearTransition, IUIAnimationTransitionLibrary2::CreateLinearTransition, uianimation.iuianimationtransitionlibrary2_createlineartransition, uianimation/IUIAnimationTransitionLibrary2::CreateLinearTransition
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
 - IUIAnimationTransitionLibrary2::CreateLinearTransition
 - uianimation/IUIAnimationTransitionLibrary2::CreateLinearTransition
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
 - IUIAnimationTransitionLibrary2.CreateLinearTransition
---

# IUIAnimationTransitionLibrary2::CreateLinearTransition


## -description

Creates a linear scalar transition.

## -parameters

### -param duration [in]

The duration of the transition.

### -param finalValue [in]

The value of the animation variable at the end of the transition.

### -param transition [out]

The new linear transition.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

During a linear transition, the value of the animation variable transitions linearly from its initial value to a  specified final value.

The following figure shows the change in value over time of an animation variable during a linear transition.

<img alt="Diagram showing a linear transition" src="Images/LinearTransition.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary2">IUIAnimationTransitionLibrary2</a>