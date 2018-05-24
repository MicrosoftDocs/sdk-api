---
UID: NF:uianimation.IUIAnimationTimerEventHandler.OnRenderingTooSlow
title: IUIAnimationTimerEventHandler::OnRenderingTooSlow
author: windows-driver-content
description: Handles events that occur when the rendering frame rate for an animation falls below a minimum desirable frame rate.
old-location: uianimation\iuianimationtimereventhandler_onrenderingtooslow.htm
old-project: UIAnimation
ms.assetid: 79986646-2d82-41a3-bff7-b2f0492c7a1b
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IUIAnimationTimerEventHandler interface [Windows Animation],OnRenderingTooSlow method, IUIAnimationTimerEventHandler.OnRenderingTooSlow, IUIAnimationTimerEventHandler::OnRenderingTooSlow, OnRenderingTooSlow, OnRenderingTooSlow method [Windows Animation], OnRenderingTooSlow method [Windows Animation],IUIAnimationTimerEventHandler interface, uianimation.iuianimationtimereventhandler_onrenderingtooslow, uianimation/IUIAnimationTimerEventHandler::OnRenderingTooSlow
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
-	IUIAnimationTimerEventHandler.OnRenderingTooSlow
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

