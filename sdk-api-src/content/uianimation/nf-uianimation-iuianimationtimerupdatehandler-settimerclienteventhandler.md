---
UID: NF:uianimation.IUIAnimationTimerUpdateHandler.SetTimerClientEventHandler
title: IUIAnimationTimerUpdateHandler::SetTimerClientEventHandler (uianimation.h)
author: windows-sdk-content
description: Specifies a handler for timer client status change events.
old-location: uianimation\iuianimationtimerupdatehandler_settimerclienteventhandler.htm
tech.root: UIAnimation
ms.assetid: ce213fc5-1329-413f-abf1-a4ab7c78818e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationTimerUpdateHandler interface [Windows Animation],SetTimerClientEventHandler method, IUIAnimationTimerUpdateHandler.SetTimerClientEventHandler, IUIAnimationTimerUpdateHandler::SetTimerClientEventHandler, SetTimerClientEventHandler, SetTimerClientEventHandler method [Windows Animation], SetTimerClientEventHandler method [Windows Animation],IUIAnimationTimerUpdateHandler interface, uianimation.iuianimationtimerupdatehandler_settimerclienteventhandler, uianimation/IUIAnimationTimerUpdateHandler::SetTimerClientEventHandler
ms.topic: method
f1_keywords: 
 - "uianimation/IUIAnimationTimerUpdateHandler.SetTimerClientEventHandler"
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
 - IUIAnimationTimerUpdateHandler.SetTimerClientEventHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationTimerUpdateHandler::SetTimerClientEventHandler


## -description


Specifies a handler for timer client status change events.


## -parameters




### -param handler [in]

A handler for timer client events.  The specified object must implement
               <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerclienteventhandler">IUIAnimationTimerUpdateHandler</a>.
            


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



If the update handler is already connected to the timer, this method returns <b>UI_E_TIMER_CLIENT_ALREADY_CONNECTED.</b>




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerupdatehandler">IUIAnimationTimerUpdateHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimerupdatehandler-cleartimerclienteventhandler">IUIAnimationTimerUpdateHandler::ClearTimerClientEventHandler</a>
 

 

