---
UID: NF:uianimation.IUIAnimationTimerEventHandler.OnRenderingTooSlow
title: IUIAnimationTimerEventHandler::OnRenderingTooSlow (uianimation.h)
description: Handles events that occur when the rendering frame rate for an animation falls below a minimum desirable frame rate.
helpviewer_keywords: ["IUIAnimationTimerEventHandler interface [Windows Animation]","OnRenderingTooSlow method","IUIAnimationTimerEventHandler.OnRenderingTooSlow","IUIAnimationTimerEventHandler::OnRenderingTooSlow","OnRenderingTooSlow","OnRenderingTooSlow method [Windows Animation]","OnRenderingTooSlow method [Windows Animation]","IUIAnimationTimerEventHandler interface","uianimation.iuianimationtimereventhandler_onrenderingtooslow","uianimation/IUIAnimationTimerEventHandler::OnRenderingTooSlow"]
old-location: uianimation\iuianimationtimereventhandler_onrenderingtooslow.htm
tech.root: UIAnimation
ms.assetid: 79986646-2d82-41a3-bff7-b2f0492c7a1b
ms.date: 12/05/2018
ms.keywords: IUIAnimationTimerEventHandler interface [Windows Animation],OnRenderingTooSlow method, IUIAnimationTimerEventHandler.OnRenderingTooSlow, IUIAnimationTimerEventHandler::OnRenderingTooSlow, OnRenderingTooSlow, OnRenderingTooSlow method [Windows Animation], OnRenderingTooSlow method [Windows Animation],IUIAnimationTimerEventHandler interface, uianimation.iuianimationtimereventhandler_onrenderingtooslow, uianimation/IUIAnimationTimerEventHandler::OnRenderingTooSlow
f1_keywords:
- uianimation/IUIAnimationTimerEventHandler.OnRenderingTooSlow
dev_langs:
- c++
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
- IUIAnimationTimerEventHandler.OnRenderingTooSlow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationTimerEventHandler::OnRenderingTooSlow


## -description


Handles events that occur when the rendering frame rate 
      for an animation falls below a minimum desirable frame rate.
   


## -parameters




### -param framesPerSecond [in]

The current frame rate, in frames per second.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/uianimation-error-codes">UIAnimation Error Codes</a> for a list of error codes.




## -remarks



The minimum desirable frame rate is specified using the <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-setframeratethreshold">IUIAnimationTimer::SetFrameRateThreshold</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-setframeratethreshold">IUIAnimationTimer::SetFrameRateThreshold</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-settimereventhandler">IUIAnimationTimer::SetTimerEventHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimereventhandler">IUIAnimationTimerEventHandler</a>
 

 

