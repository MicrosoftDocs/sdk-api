---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateSinusoidalTransitionFromRange
title: IUIAnimationTransitionLibrary::CreateSinusoidalTransitionFromRange
author: windows-driver-content
description: Creates a sinusoidal-range transition, with a specified range of oscillation.
old-location: uianimation\iuianimationtransitionlibrary_createsinusoidaltransitionfromrange.htm
old-project: UIAnimation
ms.assetid: 7164bcac-3de3-4b52-8eb3-d38156573feb
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: CreateSinusoidalTransitionFromRange, CreateSinusoidalTransitionFromRange method [Windows Animation], CreateSinusoidalTransitionFromRange method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateSinusoidalTransitionFromRange method, IUIAnimationTransitionLibrary.CreateSinusoidalTransitionFromRange, IUIAnimationTransitionLibrary::CreateSinusoidalTransitionFromRange, uianimation.iuianimationtransitionlibrary_createsinusoidaltransitionfromrange, uianimation/IUIAnimationTransitionLibrary::CreateSinusoidalTransitionFromRange
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationTransitionLibrary.CreateSinusoidalTransitionFromRange
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionLibrary::CreateSinusoidalTransitionFromRange


## -description



      Creates a sinusoidal-range  transition, with a specified range of oscillation.


## -parameters




### -param duration [in]

The duration of the transition.


### -param minimumValue [in]

The value of the animation variable at a trough of the sinusoidal wave.


### -param maximumValue [in]

The value of the animation variable at a peak of the sinusoidal wave.


### -param period [in]

The period of oscillation of the sinusoidal wave, in seconds.


### -param slope [in]

The slope at the start of the transition.


### -param transition [out]


               The new sinusoidal-range transition.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



The value of the animation variable fluctuates between the specified minimum and maximum values over the entire duration of a  sinusodial-range transition. The <i>slope</i> parameter is used to disambiguate between the two possible sine waves specified by the other parameters.

The figure below shows the effect on an animation variable over time during a sinusoidal-range transition. Passing in the <b>UI_ANIMATION_SLOPE_INCREASING</b> enumeration value yields a wave like the solid curve shown in the figure, whereas the <b>UI_ANIMATION_SLOPE_DECREASING</b> value yields a wave like the dashed curve.

<img alt="Diagram showing a sinusoidal-range transition" src="Images/SinusolidalTransitionFromRange.png"/>



## -see-also




<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a>
 

 

