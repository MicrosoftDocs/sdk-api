---
UID: NF:uianimation.IUIAnimationTimer.SetFrameRateThreshold
title: IUIAnimationTimer::SetFrameRateThreshold
author: windows-driver-content
description: Sets the frame rate below which the timer notifies the application that rendering is too slow.
old-location: uianimation\iuianimationtimer_setframeratethreshold.htm
old-project: UIAnimation
ms.assetid: 6e9b5278-a959-40a7-a4dc-88400a80b0e3
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IUIAnimationTimer interface [Windows Animation],SetFrameRateThreshold method, IUIAnimationTimer.SetFrameRateThreshold, IUIAnimationTimer::SetFrameRateThreshold, SetFrameRateThreshold, SetFrameRateThreshold method [Windows Animation], SetFrameRateThreshold method [Windows Animation],IUIAnimationTimer interface, uianimation.iuianimationtimer_setframeratethreshold, uianimation/IUIAnimationTimer::SetFrameRateThreshold
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
-	IUIAnimationTimer.SetFrameRateThreshold
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTimer::SetFrameRateThreshold


## -description



      Sets the frame rate below which the timer notifies the application that rendering is too slow.


## -parameters




### -param framesPerSecond [in]


               The minimum desirable frame rate, in frames per second.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks




         If the rendering frame rate for an animation falls below the specified frame rate, an 
         <a href="https://msdn.microsoft.com/79986646-2d82-41a3-bff7-b2f0492c7a1b">IUIAnimationTimerEventHandler::OnRenderingTooSlow</a>
         event is raised.




## -see-also




<a href="https://msdn.microsoft.com/75d29528-005e-4f49-b8ff-651b58d58fc7">IUIAnimationTimer</a>



<a href="https://msdn.microsoft.com/7d5c459e-e1f2-470b-8568-e6847acba63a">
      IUIAnimationTimerEventHandler</a>
 

 

