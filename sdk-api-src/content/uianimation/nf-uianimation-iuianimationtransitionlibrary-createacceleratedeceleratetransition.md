---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateAccelerateDecelerateTransition
title: IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition
author: windows-sdk-content
description: Creates an accelerate-decelerate transition.
old-location: uianimation\iuianimationtransitionlibrary_createacceleratedeceleratetransition.htm
old-project: UIAnimation
ms.assetid: 97a0c6cc-991b-464f-b000-1d1199c5f4de
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateAccelerateDecelerateTransition, CreateAccelerateDecelerateTransition method [Windows Animation], CreateAccelerateDecelerateTransition method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateAccelerateDecelerateTransition method, IUIAnimationTransitionLibrary.CreateAccelerateDecelerateTransition, IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition, uianimation.iuianimationtransitionlibrary_createacceleratedeceleratetransition, uianimation/IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition
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
 - IUIAnimationTransitionLibrary.CreateAccelerateDecelerateTransition
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition


## -description


Creates an accelerate-decelerate transition.


## -parameters




### -param duration [in]

The duration of the transition.


### -param finalValue [in]

The value of the animation variable at the end of the transition.


### -param accelerationRatio [in]

The ratio of the time spent accelerating to the duration.


### -param decelerationRatio [in]

The ratio of the time spent decelerating to the duration.


### -param transition [out]

The new accelerate-decelerate transition.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



During an accelerate-decelerate transition, the animation variable
      speeds up and then slows down over the duration of the transition, ending at a specified value. You can control how quickly the variable accelerates and decelerates independently, by specifying different acceleration and deceleration ratios.

When the initial velocity is zero, the acceleration ratio is the fraction of the duration that the variable will spend accelerating; likewise with the deceleration ratio. If the initial velocity is nonzero, it is the fraction of the time between the velocity reaching zero and the end of transition. The acceleration ratio and the deceleration ratio should sum to a maximum of 1.0. 

The figures below show the effect on animation variables with different initial velocities during accelerate-decelerate transitions.

<img alt="Diagram showing accellerate-decellerate transitions" src="Images/AccelerateDecelerateTransition.png"/>
<div class="alert"><b>Note</b>  d' in the above figure on the right shows the time between the velocity reaching zero and the end of the transition.</div>
<div> </div>

#### Examples

For an example, see <a href="https://msdn.microsoft.com/e2641c93-e520-4749-a98e-5a58c175fdb9">Create a Storyboard and Add Transitions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a>
 

 

