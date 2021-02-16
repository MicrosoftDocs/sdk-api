---
UID: NF:uianimation.IUIAnimationTimer.SetTimerEventHandler
title: IUIAnimationTimer::SetTimerEventHandler (uianimation.h)
description: Specifies a timer event handler.
helpviewer_keywords: ["IUIAnimationTimer interface [Windows Animation]","SetTimerEventHandler method","IUIAnimationTimer.SetTimerEventHandler","IUIAnimationTimer::SetTimerEventHandler","SetTimerEventHandler","SetTimerEventHandler method [Windows Animation]","SetTimerEventHandler method [Windows Animation]","IUIAnimationTimer interface","uianimation.iuianimationtimer_settimereventhandler","uianimation/IUIAnimationTimer::SetTimerEventHandler"]
old-location: uianimation\iuianimationtimer_settimereventhandler.htm
tech.root: UIAnimation
ms.assetid: ff1bae45-2199-4340-a27b-19865d2877f9
ms.date: 12/05/2018
ms.keywords: IUIAnimationTimer interface [Windows Animation],SetTimerEventHandler method, IUIAnimationTimer.SetTimerEventHandler, IUIAnimationTimer::SetTimerEventHandler, SetTimerEventHandler, SetTimerEventHandler method [Windows Animation], SetTimerEventHandler method [Windows Animation],IUIAnimationTimer interface, uianimation.iuianimationtimer_settimereventhandler, uianimation/IUIAnimationTimer::SetTimerEventHandler
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
 - IUIAnimationTimer::SetTimerEventHandler
 - uianimation/IUIAnimationTimer::SetTimerEventHandler
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
 - IUIAnimationTimer.SetTimerEventHandler
---

# IUIAnimationTimer::SetTimerEventHandler


## -description

Specifies a timer event handler.

## -parameters

### -param handler [in, optional]

A timer event handler.  The specified object must implement the
               <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimereventhandler">IUIAnimationTimerEventHandler</a> interface or be <b>NULL</b>. See Remarks.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Timing events include the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimereventhandler-onpreupdate">OnPreUpdate</a>,
       <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimereventhandler-onpostupdate">OnPostUpdate</a>, and
       <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimereventhandler-onrenderingtooslow">OnRenderingTooSlow</a> methods of the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimereventhandler">IUIAnimationTimerEventHandler</a> interface.

Passing <b>NULL</b> for the <i>handler</i> parameter causes Windows Animation to release its reference to any handler object you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-shutdown">IUIAnimationManager::Shutdown</a> method.


#### Examples

For an example, see <a href="/windows/desktop/UIAnimation/introducing-windows-animation-manager">Update the Animation Manager and Draw Frames</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimer">IUIAnimationTimer</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-setframeratethreshold">IUIAnimationTimer::SetFrameRateThreshold</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-settimerupdatehandler">IUIAnimationTimer::SetTimerUpdateHandler</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimereventhandler">IUIAnimationTimerEventHandler</a>