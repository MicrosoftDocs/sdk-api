---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateConstantTransition
title: IUIAnimationTransitionLibrary::CreateConstantTransition
author: windows-sdk-content
description: Creates a constant transition.
old-location: uianimation\iuianimationtransitionlibrary_createconstanttransition.htm
old-project: UIAnimation
ms.assetid: d9ad2c2d-8bcd-4730-86da-9b9432ac5b93
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CreateConstantTransition, CreateConstantTransition method [Windows Animation], CreateConstantTransition method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateConstantTransition method, IUIAnimationTransitionLibrary.CreateConstantTransition, IUIAnimationTransitionLibrary::CreateConstantTransition, uianimation.iuianimationtransitionlibrary_createconstanttransition, uianimation/IUIAnimationTransitionLibrary::CreateConstantTransition
ms.prod: windows
ms.technology: windows-sdk
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
 - IUIAnimationTransitionLibrary.CreateConstantTransition
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionLibrary::CreateConstantTransition


## -description



      Creates a constant transition.


## -parameters




### -param duration [in]


                The duration of the transition.


### -param transition [out]


                The new constant transition.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



During a constant transition, the value of an animation variable remains at the initial value over the duration of the transition.

The figure below shows the effect on an animation variable over time during a constant-duration transition.

<img alt="Diagram showing a constant-duration transition" src="Images/ConstantTransition.png"/>




## -see-also




<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a>
 

 

