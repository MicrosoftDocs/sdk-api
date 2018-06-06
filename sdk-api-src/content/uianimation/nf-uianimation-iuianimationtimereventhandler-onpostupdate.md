---
UID: NF:uianimation.IUIAnimationTimerEventHandler.OnPostUpdate
title: IUIAnimationTimerEventHandler::OnPostUpdate
author: windows-sdk-content
description: Handles events that occur after an animation update is finished.
old-location: uianimation\iuianimationtimereventhandler_onpostupdate.htm
old-project: UIAnimation
ms.assetid: 3a09537a-6cf7-4824-90c6-265dafa07a1b
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUIAnimationTimerEventHandler interface [Windows Animation],OnPostUpdate method, IUIAnimationTimerEventHandler.OnPostUpdate, IUIAnimationTimerEventHandler::OnPostUpdate, OnPostUpdate, OnPostUpdate method [Windows Animation], OnPostUpdate method [Windows Animation],IUIAnimationTimerEventHandler interface, uianimation.iuianimationtimereventhandler_onpostupdate, uianimation/IUIAnimationTimerEventHandler::OnPostUpdate
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
 - IUIAnimationTimerEventHandler.OnPostUpdate
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTimerEventHandler::OnPostUpdate


## -description



      Handles events that occur after an animation update is finished.


## -parameters






## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">UIAnimation Error Codes</a> for a list of error codes.




## -remarks



The <a href="https://msdn.microsoft.com/89e8f1be-fc4e-45e3-af7d-58556a114194">UIAnimationTimer</a> object calls this method only when calls to <a href="https://msdn.microsoft.com/06daa961-5f92-451f-958a-cf68f8ae2b0a">IUIAnimationTimerUpdateHandler::OnUpdate</a> return a result of <b>UI_ANIMATION_UPDATE_VARIABLES_CHANGED</b>.

For each tick, a timer calls the following sequence of methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/4f3dcac0-c800-48e5-82d6-b6bc3fb0409b">IUIAnimationTimerEventHandler::OnPreUpdate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/06daa961-5f92-451f-958a-cf68f8ae2b0a">IUIAnimationTimerUpdateHandler::OnUpdate</a>
</li>
<li><b>IUIAnimationTimerEventHandler::OnPostUpdate</b></li>
</ul>

<a href="https://msdn.microsoft.com/4f3dcac0-c800-48e5-82d6-b6bc3fb0409b">OnPreUpdate</a> and <b>OnPostUpdate</b> are called on the <a href="https://msdn.microsoft.com/7d5c459e-e1f2-470b-8568-e6847acba63a">IUIAnimationTimerEventHandler</a> registered with <a href="https://msdn.microsoft.com/ff1bae45-2199-4340-a27b-19865d2877f9">IUIAnimationTimer::SetTimerEventHandler</a>. <a href="https://msdn.microsoft.com/library/windows/hardware/dn926909">OnUpdate</a> is called on the <a href="https://msdn.microsoft.com/f155ed12-d493-48a0-9bdf-0e1e79cbcd38">IUIAnimationTimerUpdateHandler</a>  registered with <a href="https://msdn.microsoft.com/69c5f8b2-f3c8-43aa-8dae-cedd0036dc03">IUIAnimationTimer::SetTimerUpdateHandler</a>.




## -see-also




<a href="https://msdn.microsoft.com/ff1bae45-2199-4340-a27b-19865d2877f9">IUIAnimationTimer::SetTimerEventHandler</a>



<a href="https://msdn.microsoft.com/7d5c459e-e1f2-470b-8568-e6847acba63a">IUIAnimationTimerEventHandler</a>
 

 

