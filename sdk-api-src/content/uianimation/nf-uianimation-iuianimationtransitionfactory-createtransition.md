---
UID: NF:uianimation.IUIAnimationTransitionFactory.CreateTransition
title: IUIAnimationTransitionFactory::CreateTransition
author: windows-sdk-content
description: Creates a transition from a custom interpolator.
old-location: uianimation\iuianimationtransitionfactory_createtransition.htm
tech.root: UIAnimation
ms.assetid: 02d28669-0cbd-41e2-b9ca-4ad893f09fc9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateTransition, CreateTransition method [Windows Animation], CreateTransition method [Windows Animation],IUIAnimationTransitionFactory interface, IUIAnimationTransitionFactory interface [Windows Animation],CreateTransition method, IUIAnimationTransitionFactory.CreateTransition, IUIAnimationTransitionFactory::CreateTransition, uianimation.iuianimationtransitionfactory_createtransition, uianimation/IUIAnimationTransitionFactory::CreateTransition
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
 - IUIAnimationTransitionFactory.CreateTransition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uianimation.h
: 
- IUIAnimationTransitionFactory.CreateTransition
: 
---

# IUIAnimationTransitionFactory::CreateTransition


## -description


Creates a transition from a custom interpolator.


## -parameters




### -param interpolator [in]

The interpolator from which a transition is to be created.  
               
               The specified object must implement the
               <a href="https://msdn.microsoft.com/8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc">IUIAnimationInterpolator</a> interface.


### -param transition [out]

The new transition.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc">IUIAnimationInterpolator</a>



<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/62aec8da-e067-4b61-9465-e07fb5b42b7f">IUIAnimationTransitionFactory</a>
 

 

