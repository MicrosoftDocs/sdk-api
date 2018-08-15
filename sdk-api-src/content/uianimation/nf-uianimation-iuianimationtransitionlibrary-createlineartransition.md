---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateLinearTransition
title: IUIAnimationTransitionLibrary::CreateLinearTransition
author: windows-sdk-content
description: Creates a linear transition.
old-location: uianimation\iuianimationtransitionlibrary_createlineartransition.htm
old-project: UIAnimation
ms.assetid: 51c54bc9-771c-484e-a24f-22ba03c70709
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreateLinearTransition, CreateLinearTransition method [Windows Animation], CreateLinearTransition method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateLinearTransition method, IUIAnimationTransitionLibrary.CreateLinearTransition, IUIAnimationTransitionLibrary::CreateLinearTransition, uianimation.iuianimationtransitionlibrary_createlineartransition, uianimation/IUIAnimationTransitionLibrary::CreateLinearTransition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationTransitionLibrary.CreateLinearTransition
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionLibrary::CreateLinearTransition


## -description


Creates a linear transition.


## -parameters




### -param duration [in]

The duration of the transition.


### -param finalValue [in]

The value of the animation variable at the end of the transition.


### -param transition [out]

The new linear transition.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



During a linear transition, the value of the animation variable transitions linearly from its initial value to a  specified final value.

The figure below shows the effect on an animation variable over time during a linear transition.

<img alt="Diagram showing a linear transition" src="Images/LinearTransition.png"/>




## -see-also




<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a>
 

 

