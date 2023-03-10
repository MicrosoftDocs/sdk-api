---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateLinearVectorTransition
title: IUIAnimationTransitionLibrary2::CreateLinearVectorTransition (uianimation.h)
description: Creates a linear vector transition in the specified dimension.
helpviewer_keywords: ["CreateLinearVectorTransition","CreateLinearVectorTransition method [Windows Animation]","CreateLinearVectorTransition method [Windows Animation]","IUIAnimationTransitionLibrary2 interface","IUIAnimationTransitionLibrary2 interface [Windows Animation]","CreateLinearVectorTransition method","IUIAnimationTransitionLibrary2.CreateLinearVectorTransition","IUIAnimationTransitionLibrary2::CreateLinearVectorTransition","uianimation.iuianimationtransitionlibrary2_createlinearvectortransition","uianimation/IUIAnimationTransitionLibrary2::CreateLinearVectorTransition"]
old-location: uianimation\iuianimationtransitionlibrary2_createlinearvectortransition.htm
tech.root: UIAnimation
ms.assetid: 71A009AB-FBF3-4624-9B78-45C42B0CEE62
ms.date: 12/05/2018
ms.keywords: CreateLinearVectorTransition, CreateLinearVectorTransition method [Windows Animation], CreateLinearVectorTransition method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateLinearVectorTransition method, IUIAnimationTransitionLibrary2.CreateLinearVectorTransition, IUIAnimationTransitionLibrary2::CreateLinearVectorTransition, uianimation.iuianimationtransitionlibrary2_createlinearvectortransition, uianimation/IUIAnimationTransitionLibrary2::CreateLinearVectorTransition
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
 - IUIAnimationTransitionLibrary2::CreateLinearVectorTransition
 - uianimation/IUIAnimationTransitionLibrary2::CreateLinearVectorTransition
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
 - IUIAnimationTransitionLibrary2.CreateLinearVectorTransition
---

# IUIAnimationTransitionLibrary2::CreateLinearVectorTransition


## -description

Creates a linear vector transition in the specified dimension.

## -parameters

### -param duration [in]

The duration of the transition.

### -param finalValue [in]

A vector (of size <i>cDimension</i>) that contains  the final values of the animation variable at the end of the transition.

### -param cDimension [in]

The number of dimensions to apply the transition. This parameter specifies the number of values listed in <i>finalValue</i>.

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