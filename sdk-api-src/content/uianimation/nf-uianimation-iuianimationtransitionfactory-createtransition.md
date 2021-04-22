---
UID: NF:uianimation.IUIAnimationTransitionFactory.CreateTransition
title: IUIAnimationTransitionFactory::CreateTransition (uianimation.h)
description: Creates a transition from a custom interpolator.
helpviewer_keywords: ["CreateTransition","CreateTransition method [Windows Animation]","CreateTransition method [Windows Animation]","IUIAnimationTransitionFactory interface","IUIAnimationTransitionFactory interface [Windows Animation]","CreateTransition method","IUIAnimationTransitionFactory.CreateTransition","IUIAnimationTransitionFactory::CreateTransition","uianimation.iuianimationtransitionfactory_createtransition","uianimation/IUIAnimationTransitionFactory::CreateTransition"]
old-location: uianimation\iuianimationtransitionfactory_createtransition.htm
tech.root: UIAnimation
ms.assetid: 02d28669-0cbd-41e2-b9ca-4ad893f09fc9
ms.date: 12/05/2018
ms.keywords: CreateTransition, CreateTransition method [Windows Animation], CreateTransition method [Windows Animation],IUIAnimationTransitionFactory interface, IUIAnimationTransitionFactory interface [Windows Animation],CreateTransition method, IUIAnimationTransitionFactory.CreateTransition, IUIAnimationTransitionFactory::CreateTransition, uianimation.iuianimationtransitionfactory_createtransition, uianimation/IUIAnimationTransitionFactory::CreateTransition
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
 - IUIAnimationTransitionFactory::CreateTransition
 - uianimation/IUIAnimationTransitionFactory::CreateTransition
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
 - IUIAnimationTransitionFactory.CreateTransition
---

# IUIAnimationTransitionFactory::CreateTransition


## -description

Creates a transition from a custom interpolator.

## -parameters

### -param interpolator [in]

The interpolator from which a transition is to be created.  
               
The specified object must implement the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator">IUIAnimationInterpolator</a> interface.

### -param transition [out]

The new transition.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator">IUIAnimationInterpolator</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionfactory">IUIAnimationTransitionFactory</a>