---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateInstantaneousTransition
title: IUIAnimationTransitionLibrary2::CreateInstantaneousTransition
author: windows-driver-content
description: Creates an instantaneous scalar transition.
old-location: uianimation\iuianimationtransitionlibrary2_createinstantaneoustransition.htm
old-project: UIAnimation
ms.assetid: E40313C5-F98E-4BF3-83B8-735271ED1E2C
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: CreateInstantaneousTransition, CreateInstantaneousTransition method [Windows Animation], CreateInstantaneousTransition method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateInstantaneousTransition method, IUIAnimationTransitionLibrary2.CreateInstantaneousTransition, IUIAnimationTransitionLibrary2::CreateInstantaneousTransition, uianimation.iuianimationtransitionlibrary2_createinstantaneoustransition, uianimation/IUIAnimationTransitionLibrary2::CreateInstantaneousTransition
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
-	IUIAnimationTransitionLibrary2.CreateInstantaneousTransition
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionLibrary2::CreateInstantaneousTransition


## -description



      Creates an instantaneous scalar transition.


## -parameters




### -param finalValue [in]


               The value of the animation variable at the end of the transition.


### -param transition [out]


               The new instantaneous transition.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



During an instantaneous transition,
      the value of the animation variable changes instantly from its current value to a specified final value. The duration of this transition is always zero.

The following figure shows the change in value over time of an animation variable during an instantaneous transition.

<img alt="Diagram showing an instantaneous transition" src="Images/InstantaneousTransition.png"/>




## -see-also




<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">IUIAnimationTransition2</a>



<a href="https://msdn.microsoft.com/92C10ED5-DCE6-4B1D-8608-E2C3C6AD97BA">IUIAnimationTransitionLibrary2</a>
 

 

