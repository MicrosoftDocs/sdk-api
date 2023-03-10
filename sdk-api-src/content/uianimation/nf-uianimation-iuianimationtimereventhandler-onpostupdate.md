---
UID: NF:uianimation.IUIAnimationTimerEventHandler.OnPostUpdate
title: IUIAnimationTimerEventHandler::OnPostUpdate (uianimation.h)
description: Handles events that occur after an animation update is finished.
helpviewer_keywords: ["IUIAnimationTimerEventHandler interface [Windows Animation]","OnPostUpdate method","IUIAnimationTimerEventHandler.OnPostUpdate","IUIAnimationTimerEventHandler::OnPostUpdate","OnPostUpdate","OnPostUpdate method [Windows Animation]","OnPostUpdate method [Windows Animation]","IUIAnimationTimerEventHandler interface","uianimation.iuianimationtimereventhandler_onpostupdate","uianimation/IUIAnimationTimerEventHandler::OnPostUpdate"]
old-location: uianimation\iuianimationtimereventhandler_onpostupdate.htm
tech.root: UIAnimation
ms.assetid: 3a09537a-6cf7-4824-90c6-265dafa07a1b
ms.date: 12/05/2018
ms.keywords: IUIAnimationTimerEventHandler interface [Windows Animation],OnPostUpdate method, IUIAnimationTimerEventHandler.OnPostUpdate, IUIAnimationTimerEventHandler::OnPostUpdate, OnPostUpdate, OnPostUpdate method [Windows Animation], OnPostUpdate method [Windows Animation],IUIAnimationTimerEventHandler interface, uianimation.iuianimationtimereventhandler_onpostupdate, uianimation/IUIAnimationTimerEventHandler::OnPostUpdate
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
 - IUIAnimationTimerEventHandler::OnPostUpdate
 - uianimation/IUIAnimationTimerEventHandler::OnPostUpdate
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
 - IUIAnimationTimerEventHandler.OnPostUpdate
---

# IUIAnimationTimerEventHandler::OnPostUpdate


## -description

Handles events that occur after an animation update is finished.



## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">UIAnimation Error Codes</a> for a list of error codes.

## -remarks

The <a href="/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)">UIAnimationTimer</a> object calls this method only when calls to <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimerupdatehandler-onupdate">IUIAnimationTimerUpdateHandler::OnUpdate</a> return a result of <b>UI_ANIMATION_UPDATE_VARIABLES_CHANGED</b>.

For each tick, a timer calls the following sequence of methods:

<ul>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimereventhandler-onpreupdate">IUIAnimationTimerEventHandler::OnPreUpdate</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimerupdatehandler-onupdate">IUIAnimationTimerUpdateHandler::OnUpdate</a>
</li>
<li><b>IUIAnimationTimerEventHandler::OnPostUpdate</b></li>
</ul>

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimereventhandler-onpreupdate">OnPreUpdate</a> and <b>OnPostUpdate</b> are called on the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimereventhandler">IUIAnimationTimerEventHandler</a> registered with <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-settimereventhandler">IUIAnimationTimer::SetTimerEventHandler</a>. <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimerupdatehandler-onupdate">OnUpdate</a> is called on the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerupdatehandler">IUIAnimationTimerUpdateHandler</a>  registered with <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-settimerupdatehandler">IUIAnimationTimer::SetTimerUpdateHandler</a>.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-settimereventhandler">IUIAnimationTimer::SetTimerEventHandler</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimereventhandler">IUIAnimationTimerEventHandler</a>
