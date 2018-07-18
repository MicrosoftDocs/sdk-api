---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateSmoothStopTransition
title: IUIAnimationTransitionLibrary2::CreateSmoothStopTransition
author: windows-sdk-content
description: Creates a smooth-stop scalar transition.
old-location: uianimation\iuianimationtransitionlibrary2_createsmoothstoptransition.htm
old-project: UIAnimation
ms.assetid: 011FFBF8-31A9-4253-B034-5836B7B74409
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: CreateSmoothStopTransition, CreateSmoothStopTransition method [Windows Animation], CreateSmoothStopTransition method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateSmoothStopTransition method, IUIAnimationTransitionLibrary2.CreateSmoothStopTransition, IUIAnimationTransitionLibrary2::CreateSmoothStopTransition, uianimation.iuianimationtransitionlibrary2_createsmoothstoptransition, uianimation/IUIAnimationTransitionLibrary2::CreateSmoothStopTransition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IUIAnimationTransitionLibrary2.CreateSmoothStopTransition
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionLibrary2::CreateSmoothStopTransition


## -description



      Creates a smooth-stop scalar transition.


## -parameters




### -param maximumDuration [in]


                The maximum duration of the transition.


### -param finalValue [in]


                The value of the animation variable at the end of the transition.


### -param transition [out]


               The new smooth-stop transition.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



A smooth-stop transition slows down as it approaches the specified final value, and reaches the final value with a velocity of zero. The duration of the transition is determined by the initial velocity, the difference between the initial and final values, and the specified maximum duration. If there is no solution consisting of a single parabolic arc, this method creates a cubic transition.

The following figure shows the change in value over time of an animation variable during a smooth-stop transition.

<img alt="Diagram showing a smoth stop transition" src="Images/SmoothStopTransition.png"/>




## -see-also




<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">IUIAnimationTransition2</a>



<a href="https://msdn.microsoft.com/92C10ED5-DCE6-4B1D-8608-E2C3C6AD97BA">IUIAnimationTransitionLibrary2</a>
 

 

