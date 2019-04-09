---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateLinearTransitionFromSpeed
title: IUIAnimationTransitionLibrary2::CreateLinearTransitionFromSpeed (uianimation.h)
author: windows-sdk-content
description: Creates a linear-speed scalar transition.
old-location: uianimation\iuianimationtransitionlibrary2_createlineartransitionfromspeed.htm
tech.root: UIAnimation
ms.assetid: BCB9D6C6-6EFE-4CDF-8239-9E7E07AB53BD
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateLinearTransitionFromSpeed, CreateLinearTransitionFromSpeed method [Windows Animation], CreateLinearTransitionFromSpeed method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateLinearTransitionFromSpeed method, IUIAnimationTransitionLibrary2.CreateLinearTransitionFromSpeed, IUIAnimationTransitionLibrary2::CreateLinearTransitionFromSpeed, uianimation.iuianimationtransitionlibrary2_createlineartransitionfromspeed, uianimation/IUIAnimationTransitionLibrary2::CreateLinearTransitionFromSpeed
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
 - IUIAnimationTransitionLibrary2.CreateLinearTransitionFromSpeed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationTransitionLibrary2::CreateLinearTransitionFromSpeed


## -description


Creates a linear-speed scalar transition.


## -parameters




### -param speed [in]

The absolute value of the velocity in units/second.


### -param finalValue [in]

The value of the animation variable at the end of the transition.


### -param transition [out]

The new linear-speed transition.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



During a linear-speed transition, the value of the animation variable changes at a specified rate. The duration of the transition is determined by  the difference between the initial value and the specified final value.

The following figure shows the change in value over time of an animation variable during a linear-speed transition.

<img alt="Diagram showing the linear transition from speed" src="Images/LinearTransitionFromSpeed.png"/>




## -see-also




<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">IUIAnimationTransition2</a>



<a href="https://msdn.microsoft.com/92C10ED5-DCE6-4B1D-8608-E2C3C6AD97BA">IUIAnimationTransitionLibrary2</a>
 

 

