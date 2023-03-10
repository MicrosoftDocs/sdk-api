---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateReversalTransition
title: IUIAnimationTransitionLibrary2::CreateReversalTransition (uianimation.h)
description: Creates a reversal scalar transition.
helpviewer_keywords: ["CreateReversalTransition","CreateReversalTransition method [Windows Animation]","CreateReversalTransition method [Windows Animation]","IUIAnimationTransitionLibrary2 interface","IUIAnimationTransitionLibrary2 interface [Windows Animation]","CreateReversalTransition method","IUIAnimationTransitionLibrary2.CreateReversalTransition","IUIAnimationTransitionLibrary2::CreateReversalTransition","uianimation.iuianimationtransitionlibrary2_createreversaltransition","uianimation/IUIAnimationTransitionLibrary2::CreateReversalTransition"]
old-location: uianimation\iuianimationtransitionlibrary2_createreversaltransition.htm
tech.root: UIAnimation
ms.assetid: 49ECB93E-C253-4A7D-8181-8ED018520391
ms.date: 12/05/2018
ms.keywords: CreateReversalTransition, CreateReversalTransition method [Windows Animation], CreateReversalTransition method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateReversalTransition method, IUIAnimationTransitionLibrary2.CreateReversalTransition, IUIAnimationTransitionLibrary2::CreateReversalTransition, uianimation.iuianimationtransitionlibrary2_createreversaltransition, uianimation/IUIAnimationTransitionLibrary2::CreateReversalTransition
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
 - IUIAnimationTransitionLibrary2::CreateReversalTransition
 - uianimation/IUIAnimationTransitionLibrary2::CreateReversalTransition
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
 - IUIAnimationTransitionLibrary2.CreateReversalTransition
---

# IUIAnimationTransitionLibrary2::CreateReversalTransition


## -description

Creates a reversal scalar transition.

## -parameters

### -param duration [in]

The duration of the transition.

### -param transition [out]

The new reversal transition.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

A reversal transition smoothly changes direction over the specified duration. The final value will be the same as the initial value and the final velocity will be the negative of the initial velocity. The following figure shows such a reversal transition.

<img alt="Diagram showing a reversal transition" src="Images/ReversalTransition.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary2">IUIAnimationTransitionLibrary2</a>