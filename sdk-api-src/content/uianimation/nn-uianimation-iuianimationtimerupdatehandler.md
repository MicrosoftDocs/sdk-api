---
UID: NN:uianimation.IUIAnimationTimerUpdateHandler
title: IUIAnimationTimerUpdateHandler
author: windows-sdk-content
description: Defines methods for handling timing update events.
old-location: uianimation\iuianimationtimerupdatehandler.htm
old-project: UIAnimation
ms.assetid: f155ed12-d493-48a0-9bdf-0e1e79cbcd38
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IUIAnimationTimerUpdateHandler, IUIAnimationTimerUpdateHandler interface [Windows Animation], IUIAnimationTimerUpdateHandler interface [Windows Animation],described, uianimation.iuianimationtimerupdatehandler, uianimation/IUIAnimationTimerUpdateHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
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
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTimerUpdateHandler interface


## -description


Defines methods for handling timing update events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationTimerUpdateHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationTimerUpdateHandler</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c7383df5-dbd4-4cae-a682-47f84c2e8106">IUIAnimationTimerUpdateHandler::ClearTimerClientEventHandler</a>
</td>
<td align="left" width="63%">
Clears the handler for timer client status change events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06daa961-5f92-451f-958a-cf68f8ae2b0a">IUIAnimationTimerUpdateHandler::OnUpdate</a>
</td>
<td align="left" width="63%">
Handles update events from the timer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce213fc5-1329-413f-abf1-a4ab7c78818e">IUIAnimationTimerUpdateHandler::SetTimerClientEventHandler</a>
</td>
<td align="left" width="63%">
Specifies a handler for timer client status change events.

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/45c9c64b-9a06-4396-b715-d984655fe64c">UIAnimationManager</a> object implements this interface, so a client application can query the <b>UIAnimationManager</b> object for this interface and then pass the interface to <a href="https://msdn.microsoft.com/69c5f8b2-f3c8-43aa-8dae-cedd0036dc03">IUIAnimationTimer::SetTimerUpdateHandler</a>.  It is not necessary to disconnect the <b>UIAnimationManager</b> and <a href="https://msdn.microsoft.com/89e8f1be-fc4e-45e3-af7d-58556a114194">UIAnimationTimer</a> objects; releasing them both is sufficient to clean up.




## -see-also




<a href="https://msdn.microsoft.com/75d29528-005e-4f49-b8ff-651b58d58fc7">IUIAnimationTimer</a>



<a href="https://msdn.microsoft.com/8ca8f7d8-e698-4c55-8241-5c8f7b47f0e8">IUIAnimationTimerClientEventHandler</a>



<a href="https://msdn.microsoft.com/7d5c459e-e1f2-470b-8568-e6847acba63a">IUIAnimationTimerEventHandler</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

