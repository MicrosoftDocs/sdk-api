---
UID: NF:uianimation.IUIAnimationTimer.GetTime
title: IUIAnimationTimer::GetTime
author: windows-driver-content
description: Gets the current time.
old-location: uianimation\iuianimationtimer_gettime.htm
old-project: UIAnimation
ms.assetid: 32654e4b-158b-4d1a-afc7-98f90212b33b
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetTime, GetTime method [Windows Animation], GetTime method [Windows Animation],IUIAnimationTimer interface, IUIAnimationTimer interface [Windows Animation],GetTime method, IUIAnimationTimer.GetTime, IUIAnimationTimer::GetTime, uianimation.iuianimationtimer_gettime, uianimation/IUIAnimationTimer::GetTime
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
-	IUIAnimationTimer.GetTime
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTimer::GetTime


## -description



      Gets the current time.


## -parameters




### -param seconds [out]


               The current time, in <a href="https://msdn.microsoft.com/0745b227-61c4-462e-8529-9402c9eaa70a">UI_ANIMATION_SECONDS</a>.


## -returns




            
            If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks




         This method can be used in both the application-driven and timer-driven  configurations to retrieve the system time in <a href="https://msdn.microsoft.com/0745b227-61c4-462e-8529-9402c9eaa70a">UI_ANIMATION_SECONDS</a>, the units used throughout the Windows Animation API.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/c4f746c3-e47c-4b82-a41b-e2c0d177d097">Update the Animation Manager and Draw Frames</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/75d29528-005e-4f49-b8ff-651b58d58fc7">IUIAnimationTimer</a>



<a href="https://msdn.microsoft.com/0745b227-61c4-462e-8529-9402c9eaa70a">UI_ANIMATION_SECONDS</a>
 

 

