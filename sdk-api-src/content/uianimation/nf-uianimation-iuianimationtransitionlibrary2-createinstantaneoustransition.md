---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateInstantaneousTransition
title: IUIAnimationTransitionLibrary2::CreateInstantaneousTransition (uianimation.h)
description: Creates an instantaneous scalar transition.
helpviewer_keywords: ["CreateInstantaneousTransition","CreateInstantaneousTransition method [Windows Animation]","CreateInstantaneousTransition method [Windows Animation]","IUIAnimationTransitionLibrary2 interface","IUIAnimationTransitionLibrary2 interface [Windows Animation]","CreateInstantaneousTransition method","IUIAnimationTransitionLibrary2.CreateInstantaneousTransition","IUIAnimationTransitionLibrary2::CreateInstantaneousTransition","uianimation.iuianimationtransitionlibrary2_createinstantaneoustransition","uianimation/IUIAnimationTransitionLibrary2::CreateInstantaneousTransition"]
old-location: uianimation\iuianimationtransitionlibrary2_createinstantaneoustransition.htm
tech.root: UIAnimation
ms.assetid: E40313C5-F98E-4BF3-83B8-735271ED1E2C
ms.date: 12/05/2018
ms.keywords: CreateInstantaneousTransition, CreateInstantaneousTransition method [Windows Animation], CreateInstantaneousTransition method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateInstantaneousTransition method, IUIAnimationTransitionLibrary2.CreateInstantaneousTransition, IUIAnimationTransitionLibrary2::CreateInstantaneousTransition, uianimation.iuianimationtransitionlibrary2_createinstantaneoustransition, uianimation/IUIAnimationTransitionLibrary2::CreateInstantaneousTransition
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
 - IUIAnimationTransitionLibrary2::CreateInstantaneousTransition
 - uianimation/IUIAnimationTransitionLibrary2::CreateInstantaneousTransition
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
 - IUIAnimationTransitionLibrary2.CreateInstantaneousTransition
---

# IUIAnimationTransitionLibrary2::CreateInstantaneousTransition


## -description

Creates an instantaneous scalar transition.

## -parameters

### -param finalValue [in]

The value of the animation variable at the end of the transition.

### -param transition [out]

The new instantaneous transition.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

During an instantaneous transition,
      the value of the animation variable changes instantly from its current value to a specified final value. The duration of this transition is always zero.

The following figure shows the change in value over time of an animation variable during an instantaneous transition.

<img alt="Diagram showing an instantaneous transition" src="Images/InstantaneousTransition.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary2">IUIAnimationTransitionLibrary2</a>