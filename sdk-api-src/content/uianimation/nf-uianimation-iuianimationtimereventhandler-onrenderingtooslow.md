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

# IUIAnimationTimerEventHandler::OnRenderingTooSlow


## -description



      Handles events that occur when the rendering frame rate 
      for an animation falls below a minimum desirable frame rate.
   


## -parameters




### -param framesPerSecond [in]


               The current frame rate, in frames per second.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">UIAnimation Error Codes</a> for a list of error codes.




## -remarks




          The minimum desirable frame rate is specified using the <a href="https://msdn.microsoft.com/6e9b5278-a959-40a7-a4dc-88400a80b0e3">IUIAnimationTimer::SetFrameRateThreshold</a> method.




## -see-also




<a href="https://msdn.microsoft.com/6e9b5278-a959-40a7-a4dc-88400a80b0e3">IUIAnimationTimer::SetFrameRateThreshold</a>



<a href="https://msdn.microsoft.com/ff1bae45-2199-4340-a27b-19865d2877f9">
      IUIAnimationTimer::SetTimerEventHandler</a>



<a href="https://msdn.microsoft.com/7d5c459e-e1f2-470b-8568-e6847acba63a">IUIAnimationTimerEventHandler</a>
 

 

