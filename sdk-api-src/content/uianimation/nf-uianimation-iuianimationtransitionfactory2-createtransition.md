---
UID: NF:uianimation.IUIAnimationTransitionFactory2.CreateTransition
title: IUIAnimationTransitionFactory2::CreateTransition (uianimation.h)
description: Creates a transition from a custom interpolator for a given dimension.
helpviewer_keywords: ["CreateTransition","CreateTransition method [Windows Animation]","CreateTransition method [Windows Animation]","IUIAnimationTransitionFactory2 interface","IUIAnimationTransitionFactory2 interface [Windows Animation]","CreateTransition method","IUIAnimationTransitionFactory2.CreateTransition","IUIAnimationTransitionFactory2::CreateTransition","uianimation.iuianimationtransitionfactory2_createtransition","uianimation/IUIAnimationTransitionFactory2::CreateTransition"]
old-location: uianimation\iuianimationtransitionfactory2_createtransition.htm
tech.root: UIAnimation
ms.assetid: CFF79A6B-B2C1-4B48-8F1E-70ED2CBC567A
ms.date: 12/05/2018
ms.keywords: CreateTransition, CreateTransition method [Windows Animation], CreateTransition method [Windows Animation],IUIAnimationTransitionFactory2 interface, IUIAnimationTransitionFactory2 interface [Windows Animation],CreateTransition method, IUIAnimationTransitionFactory2.CreateTransition, IUIAnimationTransitionFactory2::CreateTransition, uianimation.iuianimationtransitionfactory2_createtransition, uianimation/IUIAnimationTransitionFactory2::CreateTransition
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
 - IUIAnimationTransitionFactory2::CreateTransition
 - uianimation/IUIAnimationTransitionFactory2::CreateTransition
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
 - IUIAnimationTransitionFactory2.CreateTransition
---

# IUIAnimationTransitionFactory2::CreateTransition


## -description

Creates a transition from a custom interpolator for a given dimension.

## -parameters

### -param interpolator [in, optional]

The interpolator from which a transition is to be created.  
               
The specified object must implement the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator2">IUIAnimationInterpolator2</a> interface.

### -param transition [out]

The new transition.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. 
            
See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator2">IUIAnimationInterpolator2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionfactory2">IUIAnimationTransitionFactory2</a>