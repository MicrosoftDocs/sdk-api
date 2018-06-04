---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

