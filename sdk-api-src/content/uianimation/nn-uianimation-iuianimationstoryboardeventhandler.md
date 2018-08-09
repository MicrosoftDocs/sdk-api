---
UID: NN:uianimation.IUIAnimationStoryboardEventHandler
title: IUIAnimationStoryboardEventHandler
author: windows-sdk-content
description: Defines methods for handling status and update events for a storyboard.
old-location: uianimation\iuianimationstoryboardeventhandler.htm
old-project: UIAnimation
ms.assetid: f43f53f9-1491-4847-89ef-e65ba98a2127
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IUIAnimationStoryboardEventHandler, IUIAnimationStoryboardEventHandler interface [Windows Animation], IUIAnimationStoryboardEventHandler interface [Windows Animation],described, uianimation.iuianimationstoryboardeventhandler, uianimation/IUIAnimationStoryboardEventHandler
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
 - IUIAnimationStoryboardEventHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboardEventHandler interface


## -description


Defines methods for handling status and update events for a storyboard.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationStoryboardEventHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationStoryboardEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationStoryboardEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1ccf0e3-64fc-444e-a27b-1a5bc1d9d6fd">OnStoryboardStatusChanged</a>
</td>
<td align="left" width="63%">
Handles events that occur when a storyboard's status changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1a6349e-9c3f-49e5-8e50-b51bf260e9be">OnStoryboardUpdated</a>
</td>
<td align="left" width="63%">
Handles events that occur when a storyboard is updated.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8ee9a17f-c57c-49df-950d-491e05ba8768">IUIAnimationStoryboard::GetStatus</a>



<a href="https://msdn.microsoft.com/8fbe8e94-8585-4adc-8643-3962aff6a031">IUIAnimationStoryboard::SetStoryboardEventHandler</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/02830092-0070-44dc-8db2-239941134473">UI_ANIMATION_STORYBOARD_STATUS</a>
 

 

