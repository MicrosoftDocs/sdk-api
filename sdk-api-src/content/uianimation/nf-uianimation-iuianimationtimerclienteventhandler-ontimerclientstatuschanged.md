---
UID: NF:uianimation.IUIAnimationTimerClientEventHandler.OnTimerClientStatusChanged
title: IUIAnimationTimerClientEventHandler::OnTimerClientStatusChanged (uianimation.h)
description: Handles events that occur when the status of the timer's client changes.
helpviewer_keywords: ["IUIAnimationTimerClientEventHandler interface [Windows Animation]","OnTimerClientStatusChanged method","IUIAnimationTimerClientEventHandler.OnTimerClientStatusChanged","IUIAnimationTimerClientEventHandler::OnTimerClientStatusChanged","OnTimerClientStatusChanged","OnTimerClientStatusChanged method [Windows Animation]","OnTimerClientStatusChanged method [Windows Animation]","IUIAnimationTimerClientEventHandler interface","uianimation.iuianimationtimerclienteventhandler_ontimerclientstatuschanged","uianimation/IUIAnimationTimerClientEventHandler::OnTimerClientStatusChanged"]
old-location: uianimation\iuianimationtimerclienteventhandler_ontimerclientstatuschanged.htm
tech.root: UIAnimation
ms.assetid: a2c161ce-937e-449a-884f-89a8a847d8aa
ms.date: 12/05/2018
ms.keywords: IUIAnimationTimerClientEventHandler interface [Windows Animation],OnTimerClientStatusChanged method, IUIAnimationTimerClientEventHandler.OnTimerClientStatusChanged, IUIAnimationTimerClientEventHandler::OnTimerClientStatusChanged, OnTimerClientStatusChanged, OnTimerClientStatusChanged method [Windows Animation], OnTimerClientStatusChanged method [Windows Animation],IUIAnimationTimerClientEventHandler interface, uianimation.iuianimationtimerclienteventhandler_ontimerclientstatuschanged, uianimation/IUIAnimationTimerClientEventHandler::OnTimerClientStatusChanged
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
 - IUIAnimationTimerClientEventHandler::OnTimerClientStatusChanged
 - uianimation/IUIAnimationTimerClientEventHandler::OnTimerClientStatusChanged
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
 - IUIAnimationTimerClientEventHandler.OnTimerClientStatusChanged
---

# IUIAnimationTimerClientEventHandler::OnTimerClientStatusChanged


## -description

Handles events that occur when the status of the timer's  client changes.

## -parameters

### -param newStatus [in]

The new status of the timer's client.

### -param previousStatus [in]

The previous status of the timer's client.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerclienteventhandler">IUIAnimationTimerClientEventHandler</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimerupdatehandler-cleartimerclienteventhandler">IUIAnimationTimerUpdateHandler::ClearTimerClientEventHandler</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimerupdatehandler-settimerclienteventhandler">IUIAnimationTimerUpdateHandler::SetTimerClientEventHandler</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_timer_client_status">UI_ANIMATION_TIMER_CLIENT_STATUS</a>