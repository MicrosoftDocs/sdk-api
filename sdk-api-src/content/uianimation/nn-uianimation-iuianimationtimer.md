---
UID: NN:uianimation.IUIAnimationTimer
title: IUIAnimationTimer (uianimation.h)
author: windows-sdk-content
description: Defines an animation timer, which provides services for managing animation timing.
old-location: uianimation\iuianimationtimer.htm
tech.root: UIAnimation
ms.assetid: 75d29528-005e-4f49-b8ff-651b58d58fc7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationTimer, IUIAnimationTimer interface [Windows Animation], IUIAnimationTimer interface [Windows Animation],described, uianimation.iuianimationtimer, uianimation/IUIAnimationTimer
ms.topic: interface
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
 - IUIAnimationTimer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationTimer interface


## -description


Defines an animation timer, which provides services for managing animation timing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationTimer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationTimer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationTimer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/981f2086-3588-4150-aa0a-c427b93ef8bb">IUIAnimationTimer::Disable</a>
</td>
<td align="left" width="63%">
Disables the animation timer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2efd694-67ff-4e6e-9a47-d0ce70dbd85a">IUIAnimationTimer::Enable</a>
</td>
<td align="left" width="63%">
Enables the animation timer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32654e4b-158b-4d1a-afc7-98f90212b33b">IUIAnimationTimer::GetTime</a>
</td>
<td align="left" width="63%">
Gets the current time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42a7e690-40bb-4795-9076-5e4bed62562d">IUIAnimationTimer::IsEnabled</a>
</td>
<td align="left" width="63%">
Determines whether the timer is currently enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e9b5278-a959-40a7-a4dc-88400a80b0e3">IUIAnimationTimer::SetFrameRateThreshold</a>
</td>
<td align="left" width="63%">
Sets the frame rate below which the timer notifies the application that rendering is too slow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff1bae45-2199-4340-a27b-19865d2877f9">IUIAnimationTimer::SetTimerEventHandler</a>
</td>
<td align="left" width="63%">
Specifies a timer event handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69c5f8b2-f3c8-43aa-8dae-cedd0036dc03">IUIAnimationTimer::SetTimerUpdateHandler</a>
</td>
<td align="left" width="63%">
Specifies a timer update handler.

</td>
</tr>
</table> 


## -remarks



A timer helps to manage animation rendering by automatically indicating the passage of a small unit of time, called a tick. In turn, ticks can trigger animation rendering or other animation events. Each animation timer provides timing for a single animation manager.

The timing system is designed to provide the necessary timing services needed to support animations and does not require applications to play an explicit role in generating the ticks. The animation timer can be set up to automatically update the animation manager for each tick without application-side handling.

An application may not need to use a timer with Windows Animation, depending on the graphics platform it is using. For example, an application drawing with Direct2D or Direct3D can synchronize to monitor's refresh rate, yielding very smooth animation. However, such applications may still find the <b>IUIAnimationTimer</b> interface useful for its <a href="https://msdn.microsoft.com/32654e4b-158b-4d1a-afc7-98f90212b33b">GetTime</a> method, which returns an accurate system time in <a href="https://msdn.microsoft.com/0745b227-61c4-462e-8529-9402c9eaa70a">UI_ANIMATION_SECONDS</a>, the units used throughout the Windows Animation API.


#### Examples

For an example that creates the animation timer object, see <a href="https://msdn.microsoft.com/4005819e-482c-4052-89f8-b8e457c0c3dc">Create the Main Animation Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8ca8f7d8-e698-4c55-8241-5c8f7b47f0e8">IUIAnimationTimerClientEventHandler</a>



<a href="https://msdn.microsoft.com/7d5c459e-e1f2-470b-8568-e6847acba63a">IUIAnimationTimerEventHandler</a>



<a href="https://msdn.microsoft.com/f155ed12-d493-48a0-9bdf-0e1e79cbcd38">IUIAnimationTimerUpdateHandler</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

