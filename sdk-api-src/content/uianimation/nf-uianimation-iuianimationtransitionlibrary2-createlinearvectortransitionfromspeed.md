---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateLinearVectorTransitionFromSpeed
title: IUIAnimationTransitionLibrary2::CreateLinearVectorTransitionFromSpeed (uianimation.h)
description: Creates a linear-speed vector transition in the specified dimension.
helpviewer_keywords: ["CreateLinearVectorTransitionFromSpeed","CreateLinearVectorTransitionFromSpeed method [Windows Animation]","CreateLinearVectorTransitionFromSpeed method [Windows Animation]","IUIAnimationTransitionLibrary2 interface","IUIAnimationTransitionLibrary2 interface [Windows Animation]","CreateLinearVectorTransitionFromSpeed method","IUIAnimationTransitionLibrary2.CreateLinearVectorTransitionFromSpeed","IUIAnimationTransitionLibrary2::CreateLinearVectorTransitionFromSpeed","uianimation.iuianimationtransitionlibrary2_createlinearvectortransitionfromspeed","uianimation/IUIAnimationTransitionLibrary2::CreateLinearVectorTransitionFromSpeed"]
old-location: uianimation\iuianimationtransitionlibrary2_createlinearvectortransitionfromspeed.htm
tech.root: UIAnimation
ms.assetid: 5CFA1E23-26A7-4139-B533-8BD325E9F1B9
ms.date: 12/05/2018
ms.keywords: CreateLinearVectorTransitionFromSpeed, CreateLinearVectorTransitionFromSpeed method [Windows Animation], CreateLinearVectorTransitionFromSpeed method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateLinearVectorTransitionFromSpeed method, IUIAnimationTransitionLibrary2.CreateLinearVectorTransitionFromSpeed, IUIAnimationTransitionLibrary2::CreateLinearVectorTransitionFromSpeed, uianimation.iuianimationtransitionlibrary2_createlinearvectortransitionfromspeed, uianimation/IUIAnimationTransitionLibrary2::CreateLinearVectorTransitionFromSpeed
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
 - IUIAnimationTransitionLibrary2::CreateLinearVectorTransitionFromSpeed
 - uianimation/IUIAnimationTransitionLibrary2::CreateLinearVectorTransitionFromSpeed
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
 - IUIAnimationTransitionLibrary2.CreateLinearVectorTransitionFromSpeed
---

# IUIAnimationTransitionLibrary2::CreateLinearVectorTransitionFromSpeed


## -description

Creates a linear-speed vector transition in the specified dimension.

## -parameters

### -param speed [in]

The absolute value of the velocity in units/second.

### -param finalValue [in]

A vector (of size <i>cDimension</i>) that contains  the final values of the animation variable at the end of the transition.

### -param cDimension [in]

The number of dimensions to apply the transition. This parameter specifies the number of values listed in <i>finalValue</i>.

### -param transition [out]

The new linear-speed transition.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

During a linear-speed transition, the value of the animation variable changes at a specified rate. The duration of the transition is determined by  the difference between the initial value and the specified final value.

The following figure shows the change in value over time of an animation variable during a linear-speed transition.

<img alt="Diagram showing the linear transition from speed" src="Images/LinearTransitionFromSpeed.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary2">IUIAnimationTransitionLibrary2</a>