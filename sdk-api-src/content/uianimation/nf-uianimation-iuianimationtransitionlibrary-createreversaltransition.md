---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateReversalTransition
title: IUIAnimationTransitionLibrary::CreateReversalTransition
author: windows-sdk-content
description: Creates a reversal transition.
old-location: uianimation\iuianimationtransitionlibrary_createreversaltransition.htm
tech.root: UIAnimation
ms.assetid: ca1d0551-333f-4fe1-b288-5ccce846d697
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateReversalTransition, CreateReversalTransition method [Windows Animation], CreateReversalTransition method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateReversalTransition method, IUIAnimationTransitionLibrary.CreateReversalTransition, IUIAnimationTransitionLibrary::CreateReversalTransition, uianimation.iuianimationtransitionlibrary_createreversaltransition, uianimation/IUIAnimationTransitionLibrary::CreateReversalTransition
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
 - IUIAnimationTransitionLibrary.CreateReversalTransition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationTransitionLibrary::CreateReversalTransition


## -description


Creates a reversal transition.


## -parameters




### -param duration [in]

The duration of the transition.


### -param transition [out]

The new reversal transition.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



A reversal transition smoothly changes direction over the specified duration. The final value will be the same as the initial value and the final velocity will be the negative of the initial velocity. The figure below shows such a reversal transition.

<img alt="Diagram showing a reversal transition" src="Images/ReversalTransition.png"/>




## -see-also




<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a>
 

 

