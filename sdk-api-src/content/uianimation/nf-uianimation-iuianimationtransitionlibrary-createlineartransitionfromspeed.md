---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateLinearTransitionFromSpeed
title: IUIAnimationTransitionLibrary::CreateLinearTransitionFromSpeed (uianimation.h)
description: Creates a linear-speed transition.
helpviewer_keywords: ["CreateLinearTransitionFromSpeed","CreateLinearTransitionFromSpeed method [Windows Animation]","CreateLinearTransitionFromSpeed method [Windows Animation]","IUIAnimationTransitionLibrary interface","IUIAnimationTransitionLibrary interface [Windows Animation]","CreateLinearTransitionFromSpeed method","IUIAnimationTransitionLibrary.CreateLinearTransitionFromSpeed","IUIAnimationTransitionLibrary::CreateLinearTransitionFromSpeed","uianimation.iuianimationtransitionlibrary_createlineartransitionfromspeed","uianimation/IUIAnimationTransitionLibrary::CreateLinearTransitionFromSpeed"]
old-location: uianimation\iuianimationtransitionlibrary_createlineartransitionfromspeed.htm
tech.root: UIAnimation
ms.assetid: 0f9ce1c0-8681-456d-8ab5-76214dc529ba
ms.date: 12/05/2018
ms.keywords: CreateLinearTransitionFromSpeed, CreateLinearTransitionFromSpeed method [Windows Animation], CreateLinearTransitionFromSpeed method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateLinearTransitionFromSpeed method, IUIAnimationTransitionLibrary.CreateLinearTransitionFromSpeed, IUIAnimationTransitionLibrary::CreateLinearTransitionFromSpeed, uianimation.iuianimationtransitionlibrary_createlineartransitionfromspeed, uianimation/IUIAnimationTransitionLibrary::CreateLinearTransitionFromSpeed
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
 - IUIAnimationTransitionLibrary::CreateLinearTransitionFromSpeed
 - uianimation/IUIAnimationTransitionLibrary::CreateLinearTransitionFromSpeed
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
 - IUIAnimationTransitionLibrary.CreateLinearTransitionFromSpeed
---

# IUIAnimationTransitionLibrary::CreateLinearTransitionFromSpeed


## -description

Creates a linear-speed transition.

## -parameters

### -param speed [in]

The absolute value of the velocity.

### -param finalValue [in]

The value of the animation variable at the end of the transition.

### -param transition [out]

The new linear-speed transition.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

During a linear-speed transition, the value of the animation variable changes at a specified rate. The duration of the transition is determined by  the difference between the initial value and the specified final value.

The figure below shows the effect on an animation variable over time during a linear-speed transition.

<img alt="Diagram showing the linear transition from speed" src="Images/LinearTransitionFromSpeed.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary">IUIAnimationTransitionLibrary</a>