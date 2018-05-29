---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateReversalTransition
title: IUIAnimationTransitionLibrary2::CreateReversalTransition
author: windows-sdk-content
description: Creates a reversal scalar transition.
old-location: uianimation\iuianimationtransitionlibrary2_createreversaltransition.htm
old-project: UIAnimation
ms.assetid: 49ECB93E-C253-4A7D-8181-8ED018520391
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CreateReversalTransition, CreateReversalTransition method [Windows Animation], CreateReversalTransition method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateReversalTransition method, IUIAnimationTransitionLibrary2.CreateReversalTransition, IUIAnimationTransitionLibrary2::CreateReversalTransition, uianimation.iuianimationtransitionlibrary2_createreversaltransition, uianimation/IUIAnimationTransitionLibrary2::CreateReversalTransition
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
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationTransitionLibrary2.CreateReversalTransition
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionLibrary2::CreateReversalTransition


## -description



      Creates a reversal scalar transition.


## -parameters




### -param duration [in]

The duration of the transition.


### -param transition [out]


               The new reversal transition.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks




         A reversal transition smoothly changes direction over the specified duration. The final value will be the same as the initial value and the final velocity will be the negative of the initial velocity. The folllowing figure shows such a reversal transition.

<img alt="Diagram showing a reversal transition" src="Images/ReversalTransition.png"/>




## -see-also




<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">IUIAnimationTransition2</a>



<a href="https://msdn.microsoft.com/92C10ED5-DCE6-4B1D-8608-E2C3C6AD97BA">IUIAnimationTransitionLibrary2</a>
 

 

