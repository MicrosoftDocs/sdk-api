---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateConstantTransition
title: IUIAnimationTransitionLibrary2::CreateConstantTransition (uianimation.h)
description: Creates a constant scalar transition.
helpviewer_keywords: ["CreateConstantTransition","CreateConstantTransition method [Windows Animation]","CreateConstantTransition method [Windows Animation]","IUIAnimationTransitionLibrary2 interface","IUIAnimationTransitionLibrary2 interface [Windows Animation]","CreateConstantTransition method","IUIAnimationTransitionLibrary2.CreateConstantTransition","IUIAnimationTransitionLibrary2::CreateConstantTransition","uianimation.iuianimationtransitionlibrary2_createconstanttransition","uianimation/IUIAnimationTransitionLibrary2::CreateConstantTransition"]
old-location: uianimation\iuianimationtransitionlibrary2_createconstanttransition.htm
tech.root: UIAnimation
ms.assetid: CC7315BB-B3EC-4B40-85B9-1AF70ABB5F77
ms.date: 12/05/2018
ms.keywords: CreateConstantTransition, CreateConstantTransition method [Windows Animation], CreateConstantTransition method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateConstantTransition method, IUIAnimationTransitionLibrary2.CreateConstantTransition, IUIAnimationTransitionLibrary2::CreateConstantTransition, uianimation.iuianimationtransitionlibrary2_createconstanttransition, uianimation/IUIAnimationTransitionLibrary2::CreateConstantTransition
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
 - IUIAnimationTransitionLibrary2::CreateConstantTransition
 - uianimation/IUIAnimationTransitionLibrary2::CreateConstantTransition
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
 - IUIAnimationTransitionLibrary2.CreateConstantTransition
---

# IUIAnimationTransitionLibrary2::CreateConstantTransition


## -description

Creates a constant scalar transition.

## -parameters

### -param duration [in]

The duration of the transition.

### -param transition [out]

The new constant transition.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

During a constant transition, the value of an animation variable remains at the initial value over the duration of the transition.

The following figure shows the change in value for an animation variable over time during a constant-duration transition.

<img alt="Diagram showing a constant-duration transition" src="Images/ConstantTransition.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary2">IUIAnimationTransitionLibrary2</a>