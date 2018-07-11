---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateLinearTransitionFromSpeed
title: IUIAnimationTransitionLibrary::CreateLinearTransitionFromSpeed
author: windows-sdk-content
description: Creates a linear-speed transition.
old-location: uianimation\iuianimationtransitionlibrary_createlineartransitionfromspeed.htm
old-project: UIAnimation
ms.assetid: 0f9ce1c0-8681-456d-8ab5-76214dc529ba
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: CreateLinearTransitionFromSpeed, CreateLinearTransitionFromSpeed method [Windows Animation], CreateLinearTransitionFromSpeed method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateLinearTransitionFromSpeed method, IUIAnimationTransitionLibrary.CreateLinearTransitionFromSpeed, IUIAnimationTransitionLibrary::CreateLinearTransitionFromSpeed, uianimation.iuianimationtransitionlibrary_createlineartransitionfromspeed, uianimation/IUIAnimationTransitionLibrary::CreateLinearTransitionFromSpeed
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps | UWP apps]
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
 - IUIAnimationTransitionLibrary.CreateLinearTransitionFromSpeed
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
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



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



During a linear-speed transition, the value of the animation variable changes at a specified rate. The duration of the transition is determined by  the difference between the initial value and the specified final value.

The figure below shows the effect on an animation variable over time during a linear-speed transition.

<img alt="Diagram showing the linear transition from speed" src="Images/LinearTransitionFromSpeed.png"/>




## -see-also




<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a>
 

 

