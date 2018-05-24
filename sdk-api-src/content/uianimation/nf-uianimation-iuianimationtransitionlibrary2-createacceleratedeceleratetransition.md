---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateAccelerateDecelerateTransition
title: IUIAnimationTransitionLibrary2::CreateAccelerateDecelerateTransition
author: windows-driver-content
description: Creates an accelerate-decelerate scalar transition.
old-location: uianimation\iuianimationtransitionlibrary2_createacceleratedeceleratetransition.htm
old-project: UIAnimation
ms.assetid: 813B4539-2942-484E-BC20-3A8178EBF9A0
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: CreateAccelerateDecelerateTransition, CreateAccelerateDecelerateTransition method [Windows Animation], CreateAccelerateDecelerateTransition method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateAccelerateDecelerateTransition method, IUIAnimationTransitionLibrary2.CreateAccelerateDecelerateTransition, IUIAnimationTransitionLibrary2::CreateAccelerateDecelerateTransition, uianimation.iuianimationtransitionlibrary2_createacceleratedeceleratetransition, uianimation/IUIAnimationTransitionLibrary2::CreateAccelerateDecelerateTransition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps | UWP apps]
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
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationTransitionLibrary2.CreateAccelerateDecelerateTransition
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionLibrary2::CreateAccelerateDecelerateTransition


## -description



      Creates an accelerate-decelerate scalar transition.


## -parameters




### -param duration [in]

The duration of the transition.


### -param finalValue [in]


                The value of the animation variable at the end of the transition.


### -param accelerationRatio [in]


               The ratio of <i>duration</i> time spent accelerating (0 to 1).


### -param decelerationRatio [in]


               The ratio of <i>duration</i> time spent decelerating (0 to 1).


### -param transition [out]


               The new accelerate-decelerate transition.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



During an accelerate-decelerate transition, the animation variable
      speeds up and then slows down over the duration of the transition, ending at a specified value. You can control how quickly the variable accelerates and decelerates independently, by specifying different acceleration and deceleration ratios.

When the initial velocity is zero, the acceleration ratio is the fraction of the duration that the variable will spend accelerating; likewise for the deceleration ratio. If the value of initial velocity is nonzero, the value is the fraction of the time between the velocity reaching zero and the end of transition. The acceleration ratio and the deceleration ratio should sum to a maximum of 1.0. 

The following figures show the change in value for animation variables with different initial velocities during accelerate-decelerate transitions.

<img alt="Diagram showing accelerate-decelerate transitions" src="Images/AccelerateDecelerateTransition.png"/>
<div class="alert"><b>Note</b>  d' in the figure on the right shows the time between the velocity reaching zero and the end of the transition.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">IUIAnimationTransition2</a>



<a href="https://msdn.microsoft.com/92C10ED5-DCE6-4B1D-8608-E2C3C6AD97BA">IUIAnimationTransitionLibrary2</a>
 

 

