---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateParabolicTransitionFromAcceleration
title: IUIAnimationTransitionLibrary2::CreateParabolicTransitionFromAcceleration
author: windows-sdk-content
description: Creates a parabolic-acceleration scalar transition.
old-location: uianimation\iuianimationtransitionlibrary2_createparabolictransitionfromacceleration.htm
old-project: UIAnimation
ms.assetid: C2005144-CA40-4835-8AFA-7E87AE99867F
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreateParabolicTransitionFromAcceleration, CreateParabolicTransitionFromAcceleration method [Windows Animation], CreateParabolicTransitionFromAcceleration method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateParabolicTransitionFromAcceleration method, IUIAnimationTransitionLibrary2.CreateParabolicTransitionFromAcceleration, IUIAnimationTransitionLibrary2::CreateParabolicTransitionFromAcceleration, uianimation.iuianimationtransitionlibrary2_createparabolictransitionfromacceleration, uianimation/IUIAnimationTransitionLibrary2::CreateParabolicTransitionFromAcceleration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.redist: 
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
 - IUIAnimationTransitionLibrary2.CreateParabolicTransitionFromAcceleration
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionLibrary2::CreateParabolicTransitionFromAcceleration


## -description


Creates a parabolic-acceleration scalar transition.


## -parameters




### -param finalValue [in]

The value of the animation variable at the end of the transition.


### -param finalVelocity [in]

The velocity, in units/second, at the end of the transition.


### -param acceleration [in]

The acceleration, in units/second², during the transition.


### -param transition [out]

The new parabolic-acceleration transition.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



During a parabolic-acceleration transition, the value of the animation variable changes from the  initial value to the final value, ending at the specified velocity.  You can control how quickly the variable reaches the final value by specifying the rate of acceleration.

The following figure shows the change in value over time of an animation variable during a parabolic-acceleration transition.

<img alt="Diagram showing a parabolic-acceleration transition" src="Images/ParabolicTransitionFromAcceleration.png"/>



## -see-also




<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">IUIAnimationTransition2</a>



<a href="https://msdn.microsoft.com/92C10ED5-DCE6-4B1D-8608-E2C3C6AD97BA">IUIAnimationTransitionLibrary2</a>
 

 

