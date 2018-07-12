---
UID: NF:uianimation.IUIAnimationTimer.SetTimerUpdateHandler
title: IUIAnimationTimer::SetTimerUpdateHandler
author: windows-sdk-content
description: Specifies a timer update handler.
old-location: uianimation\iuianimationtimer_settimerupdatehandler.htm
old-project: UIAnimation
ms.assetid: 69c5f8b2-f3c8-43aa-8dae-cedd0036dc03
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IUIAnimationTimer interface [Windows Animation],SetTimerUpdateHandler method, IUIAnimationTimer.SetTimerUpdateHandler, IUIAnimationTimer::SetTimerUpdateHandler, SetTimerUpdateHandler, SetTimerUpdateHandler method [Windows Animation], SetTimerUpdateHandler method [Windows Animation],IUIAnimationTimer interface, uianimation.iuianimationtimer_settimerupdatehandler, uianimation/IUIAnimationTimer::SetTimerUpdateHandler
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
 - IUIAnimationTimer.SetTimerUpdateHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTimer::SetTimerUpdateHandler


## -description



      Specifies a timer update handler.


## -parameters




### -param updateHandler [in, optional]


               A timer update handler, or <b>NULL</b> (see Remarks).  The specified object must implement the
               <a href="https://msdn.microsoft.com/f155ed12-d493-48a0-9bdf-0e1e79cbcd38">IUIAnimationTimerUpdateHandler</a> interface.


### -param idleBehavior [in]


               A member of 
               <a href="https://msdn.microsoft.com/70016fbd-060c-4f2a-89d3-d474850f9d01">UI_ANIMATION_IDLE_BEHAVIOR</a> 
               that specifies the behavior of the timer when it is idle.


## -returns



If the method succeeds, it returns S_OK. If the update handler is already connected to a timer, this method returns <b>UI_E_TIMER_CLIENT_ALREADY_CONNECTED</b>. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks




      The timer update handler receives time updates (ticks) from the timer. The timer indicates an update by calling 
      the <a href="https://msdn.microsoft.com/06daa961-5f92-451f-958a-cf68f8ae2b0a">IUIAnimationTimerUpdateHandler::OnUpdate</a>      
      method on the specified handler.

Passing <b>NULL</b> for the <i>updateHandler</i> parameter causes Windows Animation to release its reference to any handler object you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="https://msdn.microsoft.com/3bcce52c-d29a-423c-ae76-eb88cbe8c8df">IUIAnimationManager::Shutdown</a> method.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/c4f746c3-e47c-4b82-a41b-e2c0d177d097">Update the Animation Manager</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/75d29528-005e-4f49-b8ff-651b58d58fc7">IUIAnimationTimer</a>



<a href="https://msdn.microsoft.com/ff1bae45-2199-4340-a27b-19865d2877f9">
      IUIAnimationTimer::SetTimerEventHandler</a>



<a href="https://msdn.microsoft.com/f155ed12-d493-48a0-9bdf-0e1e79cbcd38">IUIAnimationTimerUpdateHandler</a>
 

 

