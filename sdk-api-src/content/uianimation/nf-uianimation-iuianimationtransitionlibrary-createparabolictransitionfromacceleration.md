---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateParabolicTransitionFromAcceleration
title: IUIAnimationTransitionLibrary::CreateParabolicTransitionFromAcceleration
author: windows-sdk-content
description: Creates a parabolic-acceleration transition.
old-location: uianimation\iuianimationtransitionlibrary_createparabolictransitionfromacceleration.htm
tech.root: UIAnimation
ms.assetid: 96dd5287-36b1-4620-88ae-a52b252620d2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateParabolicTransitionFromAcceleration, CreateParabolicTransitionFromAcceleration method [Windows Animation], CreateParabolicTransitionFromAcceleration method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateParabolicTransitionFromAcceleration method, IUIAnimationTransitionLibrary.CreateParabolicTransitionFromAcceleration, IUIAnimationTransitionLibrary::CreateParabolicTransitionFromAcceleration, uianimation.iuianimationtransitionlibrary_createparabolictransitionfromacceleration, uianimation/IUIAnimationTransitionLibrary::CreateParabolicTransitionFromAcceleration
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
 - IUIAnimationTransitionLibrary.CreateParabolicTransitionFromAcceleration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationTransitionLibrary::CreateParabolicTransitionFromAcceleration


## -description


Creates a parabolic-acceleration transition.


## -parameters




### -param finalValue [in]

The value of the animation variable at the end of the transition.


### -param finalVelocity [in]

The velocity at the end of the transition.


### -param acceleration [in]

The acceleration during the transition.


### -param transition [out]

The new parabolic-acceleration transition.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



During a parabolic-acceleration transition, the value of the animation variable changes from the  initial value to the final value ending at the specified velocity.  You can control how quickly the variable reaches the final value by specifying the rate of acceleration.

The figure below shows the effect on an animation variable over time during a parabolic-acceleration transition.

<img alt="Diagram showing a parabolic-acceleration transition" src="Images/ParabolicTransitionFromAcceleration.png"/>



## -see-also




<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a>
 

 

