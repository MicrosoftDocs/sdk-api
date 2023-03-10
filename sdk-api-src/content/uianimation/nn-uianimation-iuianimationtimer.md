---
UID: NN:uianimation.IUIAnimationTimer
title: IUIAnimationTimer (uianimation.h)
description: Defines an animation timer, which provides services for managing animation timing.
helpviewer_keywords: ["IUIAnimationTimer","IUIAnimationTimer interface [Windows Animation]","IUIAnimationTimer interface [Windows Animation]","described","uianimation.iuianimationtimer","uianimation/IUIAnimationTimer"]
old-location: uianimation\iuianimationtimer.htm
tech.root: UIAnimation
ms.assetid: 75d29528-005e-4f49-b8ff-651b58d58fc7
ms.date: 12/05/2018
ms.keywords: IUIAnimationTimer, IUIAnimationTimer interface [Windows Animation], IUIAnimationTimer interface [Windows Animation],described, uianimation.iuianimationtimer, uianimation/IUIAnimationTimer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAnimationTimer
 - uianimation/IUIAnimationTimer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationTimer
---

# IUIAnimationTimer interface


## -description

Defines an animation timer, which provides services for managing animation timing.

## -inheritance

The <b>IUIAnimationTimer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationTimer</b> also has these types of members:

## -remarks

A timer helps to manage animation rendering by automatically indicating the passage of a small unit of time, called a tick. In turn, ticks can trigger animation rendering or other animation events. Each animation timer provides timing for a single animation manager.

The timing system is designed to provide the necessary timing services needed to support animations and does not require applications to play an explicit role in generating the ticks. The animation timer can be set up to automatically update the animation manager for each tick without application-side handling.

An application may not need to use a timer with Windows Animation, depending on the graphics platform it is using. For example, an application drawing with Direct2D or Direct3D can synchronize to monitor's refresh rate, yielding very smooth animation. However, such applications may still find the <b>IUIAnimationTimer</b> interface useful for its <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-gettime">GetTime</a> method, which returns an accurate system time in <a href="/windows/desktop/UIAnimation/ui-animation-seconds">UI_ANIMATION_SECONDS</a>, the units used throughout the Windows Animation API.


#### Examples

For an example that creates the animation timer object, see <a href="/windows/desktop/UIAnimation/adding-animation-to-an-application">Create the Main Animation Objects</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerclienteventhandler">IUIAnimationTimerClientEventHandler</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimereventhandler">IUIAnimationTimerEventHandler</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerupdatehandler">IUIAnimationTimerUpdateHandler</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
