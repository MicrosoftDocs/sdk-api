---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateDiscreteVectorTransition
title: IUIAnimationTransitionLibrary2::CreateDiscreteVectorTransition
author: windows-sdk-content
description: Creates a discrete vector transition for each specified dimension.
old-location: uianimation\iuianimationtransitionlibrary2_creatediscretevectortransition.htm
old-project: UIAnimation
ms.assetid: 8580FED2-7F39-4EA8-B2C5-CDB887121359
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CreateDiscreteVectorTransition, CreateDiscreteVectorTransition method [Windows Animation], CreateDiscreteVectorTransition method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateDiscreteVectorTransition method, IUIAnimationTransitionLibrary2.CreateDiscreteVectorTransition, IUIAnimationTransitionLibrary2::CreateDiscreteVectorTransition, uianimation.iuianimationtransitionlibrary2_creatediscretevectortransition, uianimation/IUIAnimationTransitionLibrary2::CreateDiscreteVectorTransition
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationTransitionLibrary2.CreateDiscreteVectorTransition
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionLibrary2::CreateDiscreteVectorTransition


## -description



      Creates a discrete vector transition for each specified dimension.


## -parameters




### -param delay [in]

The amount of time by which to delay the instantaneous switch to the final value.


### -param finalValue [in]

A vector (of size <i>cDimension</i>) that contains  the final values of the animation variable at the end of the transition.


### -param cDimension [in]

The number of dimensions to apply the transition. This parameter specifies the number of values listed in <i>finalValue</i>.


### -param hold [in]

The amount of time by which to hold the variable at its final value.


### -param transition [out]


               The new discrete transition.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



During a discrete transition, the animation variable remains at the initial value for a specified delay time, then switches instantaneously to a specified final value and remains at that value for a given hold time.

The following figure shows the change in value over time of an animation variable during a discrete transition.

<img alt="Diagram showing a discrete transition" src="Images/DiscreteTransition.png"/>




## -see-also




<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">IUIAnimationTransition2</a>



<a href="https://msdn.microsoft.com/92C10ED5-DCE6-4B1D-8608-E2C3C6AD97BA">IUIAnimationTransitionLibrary2</a>
 

 

