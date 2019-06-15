---
UID: NF:uianimation.IUIAnimationTimerEventHandler.OnPreUpdate
title: IUIAnimationTimerEventHandler::OnPreUpdate (uianimation.h)
author: windows-sdk-content
description: Handles events that occur before an animation update begins.
old-location: uianimation\iuianimationtimereventhandler_onpreupdate.htm
tech.root: UIAnimation
ms.assetid: 4f3dcac0-c800-48e5-82d6-b6bc3fb0409b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationTimerEventHandler interface [Windows Animation],OnPreUpdate method, IUIAnimationTimerEventHandler.OnPreUpdate, IUIAnimationTimerEventHandler::OnPreUpdate, OnPreUpdate, OnPreUpdate method [Windows Animation], OnPreUpdate method [Windows Animation],IUIAnimationTimerEventHandler interface, uianimation.iuianimationtimereventhandler_onpreupdate, uianimation/IUIAnimationTimerEventHandler::OnPreUpdate
ms.topic: method
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
 - IUIAnimationTimerEventHandler.OnPreUpdate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationTimerEventHandler::OnPreUpdate


## -description


Handles events that occur before an animation update begins.


## -parameters






## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/uianimation-error-codes">UIAnimation Error Codes</a> for a list of error codes.




## -remarks



For each tick, a timer calls the following sequence of methods:

<ul>
<li><b>IUIAnimationTimerEventHandler::OnPreUpdate</b></li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimerupdatehandler-onupdate">IUIAnimationTimerUpdateHandler::OnUpdate</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimereventhandler-onpostupdate">IUIAnimationTimerEventHandler::OnPostUpdate</a>
</li>
</ul>
<b>OnPreUpdate</b> and <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimereventhandler-onpostupdate">OnPostUpdate</a> are called on the <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimereventhandler">IUIAnimationTimerEventHandler</a> registered with the <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-settimereventhandler">IUIAnimationTimer::SetTimerEventHandler</a> method. <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimerupdatehandler-onupdate">OnUpdate</a> is called on the <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerupdatehandler">IUIAnimationTimerUpdateHandler</a>  registered with the <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-settimerupdatehandler">IUIAnimationTimer::SetTimerUpdateHandler</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimereventhandler">IUIAnimationTimerEventHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-settimereventhandler">SetTimerEventHandler</a>
 

 

