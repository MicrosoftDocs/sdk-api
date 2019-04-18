---
UID: NF:uianimation.IUIAnimationTimer.SetTimerEventHandler
title: IUIAnimationTimer::SetTimerEventHandler (uianimation.h)
author: windows-sdk-content
description: Specifies a timer event handler.
old-location: uianimation\iuianimationtimer_settimereventhandler.htm
tech.root: UIAnimation
ms.assetid: ff1bae45-2199-4340-a27b-19865d2877f9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationTimer interface [Windows Animation],SetTimerEventHandler method, IUIAnimationTimer.SetTimerEventHandler, IUIAnimationTimer::SetTimerEventHandler, SetTimerEventHandler, SetTimerEventHandler method [Windows Animation], SetTimerEventHandler method [Windows Animation],IUIAnimationTimer interface, uianimation.iuianimationtimer_settimereventhandler, uianimation/IUIAnimationTimer::SetTimerEventHandler
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
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationTimer.SetTimerEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationTimer::SetTimerEventHandler


## -description


Specifies a timer event handler.


## -parameters




### -param handler [in, optional]

A timer event handler.  The specified object must implement the
               <a href="https://msdn.microsoft.com/7d5c459e-e1f2-470b-8568-e6847acba63a">IUIAnimationTimerEventHandler</a> interface or be <b>NULL</b>. See Remarks.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Timing events include the <a href="https://msdn.microsoft.com/4f3dcac0-c800-48e5-82d6-b6bc3fb0409b">OnPreUpdate</a>,
       <a href="https://msdn.microsoft.com/3a09537a-6cf7-4824-90c6-265dafa07a1b">OnPostUpdate</a>, and
       <a href="https://msdn.microsoft.com/79986646-2d82-41a3-bff7-b2f0492c7a1b">OnRenderingTooSlow</a> methods of the <a href="https://msdn.microsoft.com/7d5c459e-e1f2-470b-8568-e6847acba63a">IUIAnimationTimerEventHandler</a> interface.

Passing <b>NULL</b> for the <i>handler</i> parameter causes Windows Animation to release its reference to any handler object you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="https://msdn.microsoft.com/3bcce52c-d29a-423c-ae76-eb88cbe8c8df">IUIAnimationManager::Shutdown</a> method.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/c4f746c3-e47c-4b82-a41b-e2c0d177d097">Update the Animation Manager and Draw Frames</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/75d29528-005e-4f49-b8ff-651b58d58fc7">IUIAnimationTimer</a>



<a href="https://msdn.microsoft.com/6e9b5278-a959-40a7-a4dc-88400a80b0e3">IUIAnimationTimer::SetFrameRateThreshold</a>



<a href="https://msdn.microsoft.com/69c5f8b2-f3c8-43aa-8dae-cedd0036dc03">IUIAnimationTimer::SetTimerUpdateHandler</a>



<a href="https://msdn.microsoft.com/7d5c459e-e1f2-470b-8568-e6847acba63a">IUIAnimationTimerEventHandler</a>
 

 

