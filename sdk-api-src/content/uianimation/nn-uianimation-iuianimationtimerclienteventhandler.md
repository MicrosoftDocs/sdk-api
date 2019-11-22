---
UID: NN:uianimation.IUIAnimationTimerClientEventHandler
title: IUIAnimationTimerClientEventHandler (uianimation.h)

description: Defines a method for handling events related to changes in timer client status.
old-location: uianimation\iuianimationtimerclienteventhandler.htm
tech.root: UIAnimation
ms.assetid: 8ca8f7d8-e698-4c55-8241-5c8f7b47f0e8

ms.date: 12/05/2018
ms.keywords: IUIAnimationTimerClientEventHandler, IUIAnimationTimerClientEventHandler interface [Windows Animation], IUIAnimationTimerClientEventHandler interface [Windows Animation],described, uianimation.iuianimationtimerclienteventhandler, uianimation/IUIAnimationTimerClientEventHandler
ms.topic: interface
f1_keywords: 
 - "uianimation/IUIAnimationTimerClientEventHandler"
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
 - IUIAnimationTimerClientEventHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationTimerClientEventHandler interface


## -description


Defines a method for handling events related to changes in timer client status.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationTimerClientEventHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationTimerClientEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationTimerClientEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimerclienteventhandler-ontimerclientstatuschanged">IUIAnimationTimerClientEventHandler::OnTimerClientStatusChanged</a>
</td>
<td align="left" width="63%">
Handles events that occur when the status of the timer's  client changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimer">IUIAnimationTimer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimerupdatehandler-cleartimerclienteventhandler">IUIAnimationTimerUpdateHandler::ClearTimerClientEventHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimerupdatehandler-settimerclienteventhandler">IUIAnimationTimerUpdateHandler::SetTimerClientEventHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

