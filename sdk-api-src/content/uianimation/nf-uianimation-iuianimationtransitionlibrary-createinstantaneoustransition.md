---
UID: NF:uianimation.IUIAnimationTransitionLibrary.CreateInstantaneousTransition
title: IUIAnimationTransitionLibrary::CreateInstantaneousTransition
author: windows-sdk-content
description: Creates an instantaneous transition.
old-location: uianimation\iuianimationtransitionlibrary_createinstantaneoustransition.htm
tech.root: UIAnimation
ms.assetid: 70db1315-df4a-472e-8d79-61bf93980337
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateInstantaneousTransition, CreateInstantaneousTransition method [Windows Animation], CreateInstantaneousTransition method [Windows Animation],IUIAnimationTransitionLibrary interface, IUIAnimationTransitionLibrary interface [Windows Animation],CreateInstantaneousTransition method, IUIAnimationTransitionLibrary.CreateInstantaneousTransition, IUIAnimationTransitionLibrary::CreateInstantaneousTransition, uianimation.iuianimationtransitionlibrary_createinstantaneoustransition, uianimation/IUIAnimationTransitionLibrary::CreateInstantaneousTransition
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
 - IUIAnimationTransitionLibrary.CreateInstantaneousTransition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationTransitionLibrary::CreateInstantaneousTransition


## -description


Creates an instantaneous transition.


## -parameters




### -param finalValue [in]

The value of the animation variable at the end of the transition.


### -param transition [out]

The new instantaneous transition.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



During an instantaneous transition,
      the value of the animation variable changes instantly from its current value to a specified final value. The duration of this transition is always zero.

The figure below shows the effect on an animation variable over time during an instantaneous transition.

<img alt="Diagram showing an instantaneous transition" src="Images/InstantaneousTransition.png"/>




## -see-also




<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a>
 

 

