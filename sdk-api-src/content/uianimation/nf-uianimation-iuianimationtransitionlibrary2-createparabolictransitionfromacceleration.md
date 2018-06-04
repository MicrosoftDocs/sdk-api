---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

