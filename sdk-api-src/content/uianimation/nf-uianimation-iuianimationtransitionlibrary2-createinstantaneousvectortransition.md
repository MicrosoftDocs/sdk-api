---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateInstantaneousVectorTransition
title: IUIAnimationTransitionLibrary2::CreateInstantaneousVectorTransition (uianimation.h)
description: Creates an instantaneous vector transition for each specified dimension.
helpviewer_keywords: ["CreateInstantaneousVectorTransition","CreateInstantaneousVectorTransition method [Windows Animation]","CreateInstantaneousVectorTransition method [Windows Animation]","IUIAnimationTransitionLibrary2 interface","IUIAnimationTransitionLibrary2 interface [Windows Animation]","CreateInstantaneousVectorTransition method","IUIAnimationTransitionLibrary2.CreateInstantaneousVectorTransition","IUIAnimationTransitionLibrary2::CreateInstantaneousVectorTransition","uianimation.iuianimationtransitionlibrary2_createinstantaneousvectortransition","uianimation/IUIAnimationTransitionLibrary2::CreateInstantaneousVectorTransition"]
old-location: uianimation\iuianimationtransitionlibrary2_createinstantaneousvectortransition.htm
tech.root: UIAnimation
ms.assetid: C4E97F25-85BD-4548-950D-06BD5E6C4831
ms.date: 12/05/2018
ms.keywords: CreateInstantaneousVectorTransition, CreateInstantaneousVectorTransition method [Windows Animation], CreateInstantaneousVectorTransition method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateInstantaneousVectorTransition method, IUIAnimationTransitionLibrary2.CreateInstantaneousVectorTransition, IUIAnimationTransitionLibrary2::CreateInstantaneousVectorTransition, uianimation.iuianimationtransitionlibrary2_createinstantaneousvectortransition, uianimation/IUIAnimationTransitionLibrary2::CreateInstantaneousVectorTransition
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
 - IUIAnimationTransitionLibrary2::CreateInstantaneousVectorTransition
 - uianimation/IUIAnimationTransitionLibrary2::CreateInstantaneousVectorTransition
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
 - IUIAnimationTransitionLibrary2.CreateInstantaneousVectorTransition
---

# IUIAnimationTransitionLibrary2::CreateInstantaneousVectorTransition


## -description

Creates an instantaneous vector transition for each specified dimension.

## -parameters

### -param finalValue [in]

A vector (of size <i>cDimension</i>) that contains  the values of the animation variable at the end of the transition.

### -param cDimension [in]

The number of dimensions to apply the transition. This parameter specifies the number of values listed in <i>finalValue</i>.

### -param transition [out, retval]

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