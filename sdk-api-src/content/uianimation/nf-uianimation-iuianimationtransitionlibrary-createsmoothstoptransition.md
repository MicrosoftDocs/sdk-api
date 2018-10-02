---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateSmoothStopTransition
title: IUIAnimationTransitionLibrary::CreateSmoothStopTransition
author: windows-sdk-content
description: Creates a smooth-stop transition.
old-location: uianimation\iuianimationtransitionlibrary_createsmoothstoptransition.htm
tech.root: UIAnimation
ms.assetid: fce15425-5529-4ebf-9961-7e125cc64edb
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateSmoothStopTransition, CreateSmoothStopTransition method [Windows Animation], CreateSmoothStopTransition method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateSmoothStopTransition method, IUIAnimationTransitionLibrary.CreateSmoothStopTransition, IUIAnimationTransitionLibrary::CreateSmoothStopTransition, uianimation.iuianimationtransitionlibrary_createsmoothstoptransition, uianimation/IUIAnimationTransitionLibrary::CreateSmoothStopTransition
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
 - IUIAnimationTransitionLibrary.CreateSmoothStopTransition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationTransitionLibrary::CreateSmoothStopTransition


## -description


Creates a smooth-stop transition.


## -parameters




### -param maximumDuration [in]

The maximum duration of the transition.


### -param finalValue [in]

The value of the animation variable at the end of the transition.


### -param transition [out]

The new smooth-stop transition.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



A smooth-stop transition slows down as it approaches the specified final value, and reaches it with a velocity of zero. The duration of the transition is determined by the initial velocity, the difference between the initial and final values, and the specified maximum duration. If there is no solution consisting of a single parabolic arc, this method creates a cubic transition.

The figure below shows the effect on an animation variable over time during a smooth-stop transition.

<img alt="Diagram showing a smoth stop transition" src="Images/SmoothStopTransition.png"/>




## -see-also




<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a>
 

 

