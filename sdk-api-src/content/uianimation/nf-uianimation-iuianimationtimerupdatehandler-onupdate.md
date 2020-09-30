---
UID: NF:uianimation.IUIAnimationTimerUpdateHandler.OnUpdate
title: IUIAnimationTimerUpdateHandler::OnUpdate (uianimation.h)
description: Handles update events from the timer.
helpviewer_keywords: ["IUIAnimationTimerUpdateHandler interface [Windows Animation]","OnUpdate method","IUIAnimationTimerUpdateHandler.OnUpdate","IUIAnimationTimerUpdateHandler::OnUpdate","OnUpdate","OnUpdate method [Windows Animation]","OnUpdate method [Windows Animation]","IUIAnimationTimerUpdateHandler interface","uianimation.iuianimationtimerupdatehandler_onupdate","uianimation/IUIAnimationTimerUpdateHandler::OnUpdate"]
old-location: uianimation\iuianimationtimerupdatehandler_onupdate.htm
tech.root: UIAnimation
ms.assetid: 06daa961-5f92-451f-958a-cf68f8ae2b0a
ms.date: 12/05/2018
ms.keywords: IUIAnimationTimerUpdateHandler interface [Windows Animation],OnUpdate method, IUIAnimationTimerUpdateHandler.OnUpdate, IUIAnimationTimerUpdateHandler::OnUpdate, OnUpdate, OnUpdate method [Windows Animation], OnUpdate method [Windows Animation],IUIAnimationTimerUpdateHandler interface, uianimation.iuianimationtimerupdatehandler_onupdate, uianimation/IUIAnimationTimerUpdateHandler::OnUpdate
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
 - IUIAnimationTimerUpdateHandler::OnUpdate
 - uianimation/IUIAnimationTimerUpdateHandler::OnUpdate
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
 - IUIAnimationTimerUpdateHandler.OnUpdate
---

# IUIAnimationTimerUpdateHandler::OnUpdate


## -description

Handles update events from the timer.

## -parameters

### -param timeNow [in]

The current timer time, in seconds.

### -param result [out]

 Receives a member of the <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_update_result">UI_ANIMATION_UPDATE_RESULT</a> enumeration, indicating whether any animation variables changed as a result of the update.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method is used by the <a href="/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)">UIAnimationTimer</a> object to update the state of the <a href="/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)">UIAnimationManager</a> object. The <b>UIAnimationTimer</b> object calls <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimereventhandler-onpostupdate">UIAnimationTimerEventHandler::OnPostUpdate</a> only when calls to this method return a result of <b>UI_ANIMATION_UPDATE_VARIABLES_CHANGED</b>.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimereventhandler-onpostupdate">IUIAnimationTimerEventHandler::OnPostUpdate</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimereventhandler-onpreupdate">IUIAnimationTimerEventHandler::OnPreUpdate</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerupdatehandler">IUIAnimationTimerUpdateHandler</a>