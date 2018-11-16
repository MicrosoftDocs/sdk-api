---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateCubicTransition
title: IUIAnimationTransitionLibrary::CreateCubicTransition
author: windows-sdk-content
description: Creates a cubic transition.
old-location: uianimation\iuianimationtransitionlibrary_createcubictransition.htm
tech.root: UIAnimation
ms.assetid: 5003685d-d4d7-4871-b700-4d7f38050ada
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateCubicTransition, CreateCubicTransition method [Windows Animation], CreateCubicTransition method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateCubicTransition method, IUIAnimationTransitionLibrary.CreateCubicTransition, IUIAnimationTransitionLibrary::CreateCubicTransition, uianimation.iuianimationtransitionlibrary_createcubictransition, uianimation/IUIAnimationTransitionLibrary::CreateCubicTransition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationTransitionLibrary.CreateCubicTransition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uianimation.h
: 
- IUIAnimationTransitionLibrary.CreateCubicTransition
: 
---

# IUIAnimationTransitionLibrary::CreateCubicTransition


## -description


Creates a cubic transition.


## -parameters




### -param duration [in]

The duration of the transition.


### -param finalValue [in]

The value of the animation variable at the end of the transition.


### -param finalVelocity [in]

The velocity of the variable at the end of the transition.


### -param transition [out]

The new cubic transition.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



During a cubic transition, the value of the animation variable changes from its initial value to a specified final value over the duration of the transition, ending at a specified velocity.

The figure below shows the effect on an animation variable over time during a cubic transition.

<img alt="Diagram showing a cubic transition" src="Images/CubicTransition.png"/>



## -see-also




<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a>
 

 

