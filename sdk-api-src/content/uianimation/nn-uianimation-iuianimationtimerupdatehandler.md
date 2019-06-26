---
UID: NN:uianimation.IUIAnimationTimerUpdateHandler
title: IUIAnimationTimerUpdateHandler (uianimation.h)
author: windows-sdk-content
description: Defines methods for handling timing update events.
old-location: uianimation\iuianimationtimerupdatehandler.htm
tech.root: UIAnimation
ms.assetid: f155ed12-d493-48a0-9bdf-0e1e79cbcd38
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationTimerUpdateHandler, IUIAnimationTimerUpdateHandler interface [Windows Animation], IUIAnimationTimerUpdateHandler interface [Windows Animation],described, uianimation.iuianimationtimerupdatehandler, uianimation/IUIAnimationTimerUpdateHandler
ms.topic: interface
f1_keywords: 
 - "uianimation/IUIAnimationTimerUpdateHandler"
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
 - IUIAnimationTimerUpdateHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationTimerUpdateHandler interface


## -description


Defines methods for handling timing update events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationTimerUpdateHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationTimerUpdateHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationTimerUpdateHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimerupdatehandler-cleartimerclienteventhandler">IUIAnimationTimerUpdateHandler::ClearTimerClientEventHandler</a>
</td>
<td align="left" width="63%">
Clears the handler for timer client status change events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimerupdatehandler-onupdate">IUIAnimationTimerUpdateHandler::OnUpdate</a>
</td>
<td align="left" width="63%">
Handles update events from the timer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimerupdatehandler-settimerclienteventhandler">IUIAnimationTimerUpdateHandler::SetTimerClientEventHandler</a>
</td>
<td align="left" width="63%">
Specifies a handler for timer client status change events.

</td>
</tr>
</table> 


## -remarks



The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)">UIAnimationManager</a> object implements this interface, so a client application can query the <b>UIAnimationManager</b> object for this interface and then pass the interface to <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimer-settimerupdatehandler">IUIAnimationTimer::SetTimerUpdateHandler</a>.  It is not necessary to disconnect the <b>UIAnimationManager</b> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)">UIAnimationTimer</a> objects; releasing them both is sufficient to clean up.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimer">IUIAnimationTimer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimerclienteventhandler">IUIAnimationTimerClientEventHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimereventhandler">IUIAnimationTimerEventHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

