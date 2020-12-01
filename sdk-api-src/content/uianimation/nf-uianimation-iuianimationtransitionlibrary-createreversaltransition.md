---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateReversalTransition
title: IUIAnimationTransitionLibrary::CreateReversalTransition (uianimation.h)
description: Creates a reversal transition.
helpviewer_keywords: ["CreateReversalTransition","CreateReversalTransition method [Windows Animation]","CreateReversalTransition method [Windows Animation]","IUIAnimationTransitionLibrary interface","IUIAnimationTransitionLibrary interface [Windows Animation]","CreateReversalTransition method","IUIAnimationTransitionLibrary.CreateReversalTransition","IUIAnimationTransitionLibrary::CreateReversalTransition","uianimation.iuianimationtransitionlibrary_createreversaltransition","uianimation/IUIAnimationTransitionLibrary::CreateReversalTransition"]
old-location: uianimation\iuianimationtransitionlibrary_createreversaltransition.htm
tech.root: UIAnimation
ms.assetid: ca1d0551-333f-4fe1-b288-5ccce846d697
ms.date: 12/05/2018
ms.keywords: CreateReversalTransition, CreateReversalTransition method [Windows Animation], CreateReversalTransition method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateReversalTransition method, IUIAnimationTransitionLibrary.CreateReversalTransition, IUIAnimationTransitionLibrary::CreateReversalTransition, uianimation.iuianimationtransitionlibrary_createreversaltransition, uianimation/IUIAnimationTransitionLibrary::CreateReversalTransition
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
 - IUIAnimationTransitionLibrary::CreateReversalTransition
 - uianimation/IUIAnimationTransitionLibrary::CreateReversalTransition
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
 - IUIAnimationTransitionLibrary.CreateReversalTransition
---

# IUIAnimationTransitionLibrary::CreateReversalTransition


## -description

Creates a reversal transition.

## -parameters

### -param duration [in]

The duration of the transition.

### -param transition [out]

The new reversal transition.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

A reversal transition smoothly changes direction over the specified duration. The final value will be the same as the initial value and the final velocity will be the negative of the initial velocity. The figure below shows such a reversal transition.

<img alt="Diagram showing a reversal transition" src="Images/ReversalTransition.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary">IUIAnimationTransitionLibrary</a>