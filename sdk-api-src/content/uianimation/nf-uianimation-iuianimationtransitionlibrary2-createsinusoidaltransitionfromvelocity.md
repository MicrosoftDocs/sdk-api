---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateSinusoidalTransitionFromVelocity
title: IUIAnimationTransitionLibrary2::CreateSinusoidalTransitionFromVelocity
author: windows-sdk-content
description: Creates a sinusoidal scalar transition where amplitude is determined by initial velocity.
old-location: uianimation\iuianimationtransitionlibrary2_createsinusoidaltransitionfromvelocity.htm
old-project: UIAnimation
ms.assetid: 833D3482-68BC-45DD-9073-B048E11CB801
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: CreateSinusoidalTransitionFromVelocity, CreateSinusoidalTransitionFromVelocity method [Windows Animation], CreateSinusoidalTransitionFromVelocity method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateSinusoidalTransitionFromVelocity method, IUIAnimationTransitionLibrary2.CreateSinusoidalTransitionFromVelocity, IUIAnimationTransitionLibrary2::CreateSinusoidalTransitionFromVelocity, uianimation.iuianimationtransitionlibrary2_createsinusoidaltransitionfromvelocity, uianimation/IUIAnimationTransitionLibrary2::CreateSinusoidalTransitionFromVelocity
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
 - IUIAnimationTransitionLibrary2.CreateSinusoidalTransitionFromVelocity
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionLibrary2::CreateSinusoidalTransitionFromVelocity


## -description



      Creates a sinusoidal scalar transition where amplitude is determined by initial velocity.


## -parameters




### -param duration [in]


                The duration of the transition.


### -param period [in]

The period of oscillation of the sinusoidal wave.


### -param transition [out]


                The new sinusoidal-velocity transition.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



The value of the animation variable oscillates around the initial value over the entire duration of a sinusoidal-range transition. The amplitude of the oscillation is determined by the velocity when the transition begins.

The following figure shows the change in value over time of an animation variable during a sinusoidal-velocity transition.

<img alt="Diagram showing a sinusoidal-velocity transition" src="Images/SinusolidalTransitionFromVelocity.png"/>




## -see-also




<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">IUIAnimationTransition2</a>



<a href="https://msdn.microsoft.com/92C10ED5-DCE6-4B1D-8608-E2C3C6AD97BA">IUIAnimationTransitionLibrary2</a>
 

 

