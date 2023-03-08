---
UID: NF:uianimation.IUIAnimationTimer.SetFrameRateThreshold
title: IUIAnimationTimer::SetFrameRateThreshold (uianimation.h)
description: Sets the frame rate below which the timer notifies the application that rendering is too slow.
helpviewer_keywords: ["IUIAnimationTimer interface [Windows Animation]","SetFrameRateThreshold method","IUIAnimationTimer.SetFrameRateThreshold","IUIAnimationTimer::SetFrameRateThreshold","SetFrameRateThreshold","SetFrameRateThreshold method [Windows Animation]","SetFrameRateThreshold method [Windows Animation]","IUIAnimationTimer interface","uianimation.iuianimationtimer_setframeratethreshold","uianimation/IUIAnimationTimer::SetFrameRateThreshold"]
old-location: uianimation\iuianimationtimer_setframeratethreshold.htm
tech.root: UIAnimation
ms.assetid: 6e9b5278-a959-40a7-a4dc-88400a80b0e3
ms.date: 12/05/2018
ms.keywords: IUIAnimationTimer interface [Windows Animation],SetFrameRateThreshold method, IUIAnimationTimer.SetFrameRateThreshold, IUIAnimationTimer::SetFrameRateThreshold, SetFrameRateThreshold, SetFrameRateThreshold method [Windows Animation], SetFrameRateThreshold method [Windows Animation],IUIAnimationTimer interface, uianimation.iuianimationtimer_setframeratethreshold, uianimation/IUIAnimationTimer::SetFrameRateThreshold
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
 - IUIAnimationTimer::SetFrameRateThreshold
 - uianimation/IUIAnimationTimer::SetFrameRateThreshold
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
 - IUIAnimationTimer.SetFrameRateThreshold
---

# IUIAnimationTimer::SetFrameRateThreshold


## -description

Sets the frame rate below which the timer notifies the application that rendering is too slow.

## -parameters

### -param framesPerSecond [in]

The minimum desirable frame rate, in frames per second.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

If the rendering frame rate for an animation falls below the specified frame rate, an 
         <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimereventhandler-onrenderingtooslow">IUIAnimationTimerEventHandler::OnRenderingTooSlow</a> event is raised.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimer">IUIAnimationTimer</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimereventhandler">IUIAnimationTimerEventHandler</a>