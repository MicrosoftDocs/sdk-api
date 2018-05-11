---
UID: NF:uianimation.IUIAnimationTransition2.SetInitialVectorVelocity
title: IUIAnimationTransition2::SetInitialVectorVelocity
author: windows-driver-content
description: Sets the initial velocity of the transition for each specified dimension in the animation variable.
old-location: uianimation\iuianimationtransition2_setinitialvectorvelocity.htm
old-project: UIAnimation
ms.assetid: 29EFBBE0-E877-4521-B4A7-E1828E0493B9
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IUIAnimationTransition2 interface [Windows Animation],SetInitialVectorVelocity method, IUIAnimationTransition2.SetInitialVectorVelocity, IUIAnimationTransition2::SetInitialVectorVelocity, SetInitialVectorVelocity, SetInitialVectorVelocity method [Windows Animation], SetInitialVectorVelocity method [Windows Animation],IUIAnimationTransition2 interface, uianimation.iuianimationtransition2_setinitialvectorvelocity, uianimation/IUIAnimationTransition2::SetInitialVectorVelocity
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
-	IUIAnimationTransition2.SetInitialVectorVelocity
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransition2::SetInitialVectorVelocity


## -description


Sets the initial velocity of the transition for each specified dimension in the animation variable.


## -parameters




### -param velocity [in]

A vector (of size <i>cDimension</i>) that contains  the initial velocities for the transition.


### -param cDimension [in]

The number of dimensions that require transition velocities. This parameter specifies the number of values listed in <i>velocity</i>.


## -returns



Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">IUIAnimationTransition2</a>
 

 

