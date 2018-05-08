---
UID: NF:uianimation.IUIAnimationTimerUpdateHandler.OnUpdate
title: IUIAnimationTimerUpdateHandler::OnUpdate
author: windows-driver-content
description: Handles update events from the timer.
old-location: uianimation\iuianimationtimerupdatehandler_onupdate.htm
old-project: UIAnimation
ms.assetid: 06daa961-5f92-451f-958a-cf68f8ae2b0a
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IUIAnimationTimerUpdateHandler interface [Windows Animation],OnUpdate method, IUIAnimationTimerUpdateHandler.OnUpdate, IUIAnimationTimerUpdateHandler::OnUpdate, OnUpdate, OnUpdate method [Windows Animation], OnUpdate method [Windows Animation],IUIAnimationTimerUpdateHandler interface, uianimation.iuianimationtimerupdatehandler_onupdate, uianimation/IUIAnimationTimerUpdateHandler::OnUpdate
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationTimerUpdateHandler.OnUpdate
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTimerUpdateHandler::OnUpdate


## -description



      Handles update events from the timer.


## -parameters




### -param timeNow [in]


            The current timer time, in seconds.


### -param result [out]

 Receives a member of the <a href="https://msdn.microsoft.com/19b1d80f-39b3-4046-aa6a-5312e004b4b0">UI_ANIMATION_UPDATE_RESULT</a> enumeration, indicating whether any animation variables changed as a result of the update.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method is used by the <a href="https://msdn.microsoft.com/89e8f1be-fc4e-45e3-af7d-58556a114194">UIAnimationTimer</a> object to update the state of the <a href="https://msdn.microsoft.com/45c9c64b-9a06-4396-b715-d984655fe64c">UIAnimationManager</a> object. The <b>UIAnimationTimer</b> object calls <a href="https://msdn.microsoft.com/3a09537a-6cf7-4824-90c6-265dafa07a1b">UIAnimationTimerEventHandler::OnPostUpdate</a> only when calls to this method return a result of <b>UI_ANIMATION_UPDATE_VARIABLES_CHANGED</b>.




## -see-also




<a href="https://msdn.microsoft.com/3a09537a-6cf7-4824-90c6-265dafa07a1b">
      
      IUIAnimationTimerEventHandler::OnPostUpdate</a>



<a href="https://msdn.microsoft.com/4f3dcac0-c800-48e5-82d6-b6bc3fb0409b">
      IUIAnimationTimerEventHandler::OnPreUpdate</a>



<a href="https://msdn.microsoft.com/f155ed12-d493-48a0-9bdf-0e1e79cbcd38">IUIAnimationTimerUpdateHandler</a>
 

 

