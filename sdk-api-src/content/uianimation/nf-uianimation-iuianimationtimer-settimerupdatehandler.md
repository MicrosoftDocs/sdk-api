---
UID: NF:uianimation.IUIAnimationTimer.SetTimerUpdateHandler
title: IUIAnimationTimer::SetTimerUpdateHandler (uianimation.h)
description: Specifies a timer update handler.
helpviewer_keywords: ["IUIAnimationTimer interface [Windows Animation]","SetTimerUpdateHandler method","IUIAnimationTimer.SetTimerUpdateHandler","IUIAnimationTimer::SetTimerUpdateHandler","SetTimerUpdateHandler","SetTimerUpdateHandler method [Windows Animation]","SetTimerUpdateHandler method [Windows Animation]","IUIAnimationTimer interface","uianimation.iuianimationtimer_settimerupdatehandler","uianimation/IUIAnimationTimer::SetTimerUpdateHandler"]
old-location: uianimation\iuianimationtimer_settimerupdatehandler.htm
tech.root: UIAnimation
ms.assetid: 69c5f8b2-f3c8-43aa-8dae-cedd0036dc03
ms.date: 12/05/2018
ms.keywords: IUIAnimationTimer interface [Windows Animation],SetTimerUpdateHandler method, IUIAnimationTimer.SetTimerUpdateHandler, IUIAnimationTimer::SetTimerUpdateHandler, SetTimerUpdateHandler, SetTimerUpdateHandler method [Windows Animation], SetTimerUpdateHandler method [Windows Animation],IUIAnimationTimer interface, uianimation.iuianimationtimer_settimerupdatehandler, uianimation/IUIAnimationTimer::SetTimerUpdateHandler
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
 - IUIAnimationTimer::SetTimerUpdateHandler
 - uianimation/IUIAnimationTimer::SetTimerUpdateHandler
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
 - IUIAnimationTimer.SetTimerUpdateHandler
---

# IUIAnimationTimer::SetTimerUpdateHandler


## -description

Specifies a timer update handler.

## -parameters

### -param updateHandler [in, optional]

A timer update handler, or <b>NULL</b> (see Remarks).  The specified object must implement the
               <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerupdatehandler">IUIAnimationTimerUpdateHandler</a> interface.

### -param idleBehavior [in]

A member of 
               <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_idle_behavior">UI_ANIMATION_IDLE_BEHAVIOR</a> 
               that specifies the behavior of the timer when it is idle.

## -returns

If the method succeeds, it returns S_OK. If the update handler is already connected to a timer, this method returns <b>UI_E_TIMER_CLIENT_ALREADY_CONNECTED</b>. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

The timer update handler receives time updates (ticks) from the timer. The timer indicates an update by calling 
      the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimerupdatehandler-onupdate">IUIAnimationTimerUpdateHandler::OnUpdate</a>      
      method on the specified handler.

Passing <b>NULL</b> for the <i>updateHandler</i> parameter causes Windows Animation to release its reference to any handler object you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-shutdown">IUIAnimationManager::Shutdown</a> method.


#### Examples

For an example, see <a href="/windows/desktop/UIAnimation/introducing-windows-animation-manager">Update the Animation Manager</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimer">IUIAnimationTimer</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-settimereventhandler">IUIAnimationTimer::SetTimerEventHandler</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerupdatehandler">IUIAnimationTimerUpdateHandler</a>