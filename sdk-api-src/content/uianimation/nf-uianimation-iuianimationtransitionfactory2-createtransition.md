---
UID: NF:uianimation.IUIAnimationTransitionFactory2.CreateTransition
title: IUIAnimationTransitionFactory2::CreateTransition
author: windows-sdk-content
description: Creates a transition from a custom interpolator for a given dimension.
old-location: uianimation\iuianimationtransitionfactory2_createtransition.htm
old-project: UIAnimation
ms.assetid: CFF79A6B-B2C1-4B48-8F1E-70ED2CBC567A
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: CreateTransition, CreateTransition method [Windows Animation], CreateTransition method [Windows Animation],IUIAnimationTransitionFactory2 interface, IUIAnimationTransitionFactory2 interface [Windows Animation],CreateTransition method, IUIAnimationTransitionFactory2.CreateTransition, IUIAnimationTransitionFactory2::CreateTransition, uianimation.iuianimationtransitionfactory2_createtransition, uianimation/IUIAnimationTransitionFactory2::CreateTransition
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
 - IUIAnimationTransitionFactory2.CreateTransition
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionFactory2::CreateTransition


## -description


Creates a transition from a custom interpolator for a given dimension.


## -parameters




### -param interpolator [in, optional]


               The interpolator from which a transition is to be created.  
               
               The specified object must implement the
               <a href="https://msdn.microsoft.com/EC0D1933-37C3-41E2-AB13-DA4AAF4B8F04">IUIAnimationInterpolator2</a> interface.


### -param transition [out]

The new transition.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. 
            
          See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/EC0D1933-37C3-41E2-AB13-DA4AAF4B8F04">IUIAnimationInterpolator2</a>



<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">IUIAnimationTransition2</a>



<a href="https://msdn.microsoft.com/EB829B6A-770C-486A-9BA2-4D7C8F073C8F">IUIAnimationTransitionFactory2</a>
 

 

