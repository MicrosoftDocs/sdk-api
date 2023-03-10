---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateConstantTransition
title: IUIAnimationTransitionLibrary::CreateConstantTransition (uianimation.h)
description: Creates a constant transition.
helpviewer_keywords: ["CreateConstantTransition","CreateConstantTransition method [Windows Animation]","CreateConstantTransition method [Windows Animation]","IUIAnimationTransitionLibrary interface","IUIAnimationTransitionLibrary interface [Windows Animation]","CreateConstantTransition method","IUIAnimationTransitionLibrary.CreateConstantTransition","IUIAnimationTransitionLibrary::CreateConstantTransition","uianimation.iuianimationtransitionlibrary_createconstanttransition","uianimation/IUIAnimationTransitionLibrary::CreateConstantTransition"]
old-location: uianimation\iuianimationtransitionlibrary_createconstanttransition.htm
tech.root: UIAnimation
ms.assetid: d9ad2c2d-8bcd-4730-86da-9b9432ac5b93
ms.date: 12/05/2018
ms.keywords: CreateConstantTransition, CreateConstantTransition method [Windows Animation], CreateConstantTransition method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateConstantTransition method, IUIAnimationTransitionLibrary.CreateConstantTransition, IUIAnimationTransitionLibrary::CreateConstantTransition, uianimation.iuianimationtransitionlibrary_createconstanttransition, uianimation/IUIAnimationTransitionLibrary::CreateConstantTransition
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
 - IUIAnimationTransitionLibrary::CreateConstantTransition
 - uianimation/IUIAnimationTransitionLibrary::CreateConstantTransition
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
 - IUIAnimationTransitionLibrary.CreateConstantTransition
---

# IUIAnimationTransitionLibrary::CreateConstantTransition


## -description

Creates a constant transition.

## -parameters

### -param duration [in]

The duration of the transition.

### -param transition [out]

The new constant transition.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

During a constant transition, the value of an animation variable remains at the initial value over the duration of the transition.

The figure below shows the effect on an animation variable over time during a constant-duration transition.

<img alt="Diagram showing a constant-duration transition" src="Images/ConstantTransition.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary">IUIAnimationTransitionLibrary</a>