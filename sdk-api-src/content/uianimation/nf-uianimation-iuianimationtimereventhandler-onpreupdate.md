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

# IUIAnimationTimerEventHandler::OnPreUpdate


## -description



      Handles events that occur before an animation update begins.


## -parameters






## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">UIAnimation Error Codes</a> for a list of error codes.




## -remarks



For each tick, a timer calls the following sequence of methods:

<ul>
<li><b>IUIAnimationTimerEventHandler::OnPreUpdate</b></li>
<li>
<a href="https://msdn.microsoft.com/06daa961-5f92-451f-958a-cf68f8ae2b0a">IUIAnimationTimerUpdateHandler::OnUpdate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3a09537a-6cf7-4824-90c6-265dafa07a1b">IUIAnimationTimerEventHandler::OnPostUpdate</a>
</li>
</ul>
<b>OnPreUpdate</b> and <a href="https://msdn.microsoft.com/3a09537a-6cf7-4824-90c6-265dafa07a1b">OnPostUpdate</a> are called on the <a href="https://msdn.microsoft.com/7d5c459e-e1f2-470b-8568-e6847acba63a">IUIAnimationTimerEventHandler</a> registered with the <a href="https://msdn.microsoft.com/ff1bae45-2199-4340-a27b-19865d2877f9">IUIAnimationTimer::SetTimerEventHandler</a> method. <a href="https://msdn.microsoft.com/library/windows/hardware/dn926909">OnUpdate</a> is called on the <a href="https://msdn.microsoft.com/f155ed12-d493-48a0-9bdf-0e1e79cbcd38">IUIAnimationTimerUpdateHandler</a>  registered with the <a href="https://msdn.microsoft.com/69c5f8b2-f3c8-43aa-8dae-cedd0036dc03">IUIAnimationTimer::SetTimerUpdateHandler</a> method.




## -see-also




<a href="https://msdn.microsoft.com/7d5c459e-e1f2-470b-8568-e6847acba63a">IUIAnimationTimerEventHandler</a>



<a href="https://msdn.microsoft.com/ff1bae45-2199-4340-a27b-19865d2877f9">
      SetTimerEventHandler</a>
 

 

