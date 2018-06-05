---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateSinusoidalTransitionFromRange
title: IUIAnimationTransitionLibrary2::CreateSinusoidalTransitionFromRange
author: windows-sdk-content
description: Creates a sinusoidal-range scalar transition with a specified range of oscillation.
old-location: uianimation\iuianimationtransitionlibrary2_createsinusoidaltransitionfromrange.htm
old-project: UIAnimation
ms.assetid: E4222165-4726-4C79-94A8-3CC2C72CCE42
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CreateSinusoidalTransitionFromRange, CreateSinusoidalTransitionFromRange method [Windows Animation], CreateSinusoidalTransitionFromRange method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateSinusoidalTransitionFromRange method, IUIAnimationTransitionLibrary2.CreateSinusoidalTransitionFromRange, IUIAnimationTransitionLibrary2::CreateSinusoidalTransitionFromRange, uianimation.iuianimationtransitionlibrary2_createsinusoidaltransitionfromrange, uianimation/IUIAnimationTransitionLibrary2::CreateSinusoidalTransitionFromRange
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationTransitionLibrary2.CreateSinusoidalTransitionFromRange
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionLibrary2::CreateSinusoidalTransitionFromRange


## -description



      Creates a sinusoidal-range scalar  transition with a specified range of oscillation.


## -parameters




### -param duration [in]

The duration of the transition.


### -param minimumValue [in]

The value of the animation variable at a trough of the sinusoidal wave.


### -param maximumValue [in]

The value of the animation variable at a peak of the sinusoidal wave.


### -param period [in]

The period of oscillation of the sinusoidal wave.


### -param slope [in]

The slope at the start of the transition.


### -param transition [out]


               The new sinusoidal-range transition.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



The value of the animation variable fluctuates between the specified minimum and maximum values over the entire duration of a  sinusodial-range transition. The <i>slope</i> parameter is used to disambiguate between the two possible sine waves specified by the other parameters.

The following figure shows the change in value over time of an animation variable during a sinusoidal-range transition. Passing in the <a href="https://msdn.microsoft.com/17076489-4b66-44ae-87ac-39b02da0b542">UI_ANIMATION_SLOPE_INCREASING</a> enumeration value yields a wave like the solid curve shown in the figure, whereas the <b>UI_ANIMATION_SLOPE_DECREASING</b> value yields a wave like the dashed curve.

<img alt="Diagram showing a sinusoidal-range transition" src="Images/SinusolidalTransitionFromRange.png"/>



## -see-also




<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">IUIAnimationTransition2</a>



<a href="https://msdn.microsoft.com/92C10ED5-DCE6-4B1D-8608-E2C3C6AD97BA">IUIAnimationTransitionLibrary2</a>
 

 

