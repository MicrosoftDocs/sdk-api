---
UID: NF:uianimation.IUIAnimationTransition.SetInitialVelocity
title: IUIAnimationTransition::SetInitialVelocity
author: windows-sdk-content
description: Sets the initial velocity for the transition.
old-location: uianimation\iuianimationtransition_setinitialvelocity.htm
old-project: UIAnimation
ms.assetid: adb5a173-6efa-4b1b-8e2f-1d69288653ae
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IUIAnimationTransition interface [Windows Animation],SetInitialVelocity method, IUIAnimationTransition.SetInitialVelocity, IUIAnimationTransition::SetInitialVelocity, SetInitialVelocity, SetInitialVelocity method [Windows Animation], SetInitialVelocity method [Windows Animation],IUIAnimationTransition interface, uianimation.iuianimationtransition_setinitialvelocity, uianimation/IUIAnimationTransition::SetInitialVelocity
ms.prod: windows
ms.technology: windows-sdk
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
 - IUIAnimationTransition.SetInitialVelocity
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransition::SetInitialVelocity


## -description


Sets the initial velocity for the transition.


## -parameters




### -param velocity [in]

The initial velocity for the transition.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method should not be called after the transition has been added to a storyboard.



