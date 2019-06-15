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
f1_keywords: ["uianimation/IUIAnimationTimer"]
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
ms.custom: 19H1
---

# IUIAnimationTimer interface


## -description


Defines an animation timer, which provides services for managing animation timing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationTimer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationTimer</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-disable">IUIAnimationTimer::Disable</a>
</td>
<td align="left" width="63%">
Disables the animation timer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-enable">IUIAnimationTimer::Enable</a>
</td>
<td align="left" width="63%">
Enables the animation timer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-gettime">IUIAnimationTimer::GetTime</a>
</td>
<td align="left" width="63%">
Gets the current time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-isenabled">IUIAnimationTimer::IsEnabled</a>
</td>
<td align="left" width="63%">
Determines whether the timer is currently enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-setframeratethreshold">IUIAnimationTimer::SetFrameRateThreshold</a>
</td>
<td align="left" width="63%">
Sets the frame rate below which the timer notifies the application that rendering is too slow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-settimereventhandler">IUIAnimationTimer::SetTimerEventHandler</a>
</td>
<td align="left" width="63%">
Specifies a timer event handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-settimerupdatehandler">IUIAnimationTimer::SetTimerUpdateHandler</a>
</td>
<td align="left" width="63%">
Specifies a timer update handler.

</td>
</tr>
</table> 


## -remarks



A timer helps to manage animation rendering by automatically indicating the passage of a small unit of time, called a tick. In turn, ticks can trigger animation rendering or other animation events. Each animation timer provides timing for a single animation manager.

The timing system is designed to provide the necessary timing services needed to support animations and does not require applications to play an explicit role in generating the ticks. The animation timer can be set up to automatically update the animation manager for each tick without application-side handling.

An application may not need to use a timer with Windows Animation, depending on the graphics platform it is using. For example, an application drawing with Direct2D or Direct3D can synchronize to monitor's refresh rate, yielding very smooth animation. However, such applications may still find the <b>IUIAnimationTimer</b> interface useful for its <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-gettime">GetTime</a> method, which returns an accurate system time in <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/ui-animation-seconds">UI_ANIMATION_SECONDS</a>, the units used throughout the Windows Animation API.


#### Examples

For an example that creates the animation timer object, see <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/adding-animation-to-an-application">Create the Main Animation Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerclienteventhandler">IUIAnimationTimerClientEventHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimereventhandler">IUIAnimationTimerEventHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerupdatehandler">IUIAnimationTimerUpdateHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

