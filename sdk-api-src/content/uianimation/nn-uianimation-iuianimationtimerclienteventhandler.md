---
UID: NN:uianimation.IUIAnimationTimerClientEventHandler
title: IUIAnimationTimerClientEventHandler
author: windows-sdk-content
description: Defines a method for handling events related to changes in timer client status.
old-location: uianimation\iuianimationtimerclienteventhandler.htm
old-project: UIAnimation
ms.assetid: 8ca8f7d8-e698-4c55-8241-5c8f7b47f0e8
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUIAnimationTimerClientEventHandler, IUIAnimationTimerClientEventHandler interface [Windows Animation], IUIAnimationTimerClientEventHandler interface [Windows Animation],described, uianimation.iuianimationtimerclienteventhandler, uianimation/IUIAnimationTimerClientEventHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps | UWP apps]
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationTimerClientEventHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTimerClientEventHandler interface


## -description



      Defines a method for handling events related to changes in timer client status.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationTimerClientEventHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationTimerClientEventHandler</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a2c161ce-937e-449a-884f-89a8a847d8aa">IUIAnimationTimerClientEventHandler::OnTimerClientStatusChanged</a>
</td>
<td align="left" width="63%">

      Handles events that occur when the status of the timer's  client changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/75d29528-005e-4f49-b8ff-651b58d58fc7">
      IUIAnimationTimer</a>



<a href="https://msdn.microsoft.com/c7383df5-dbd4-4cae-a682-47f84c2e8106">
      IUIAnimationTimerUpdateHandler::ClearTimerClientEventHandler</a>



<a href="https://msdn.microsoft.com/ce213fc5-1329-413f-abf1-a4ab7c78818e">
      IUIAnimationTimerUpdateHandler::SetTimerClientEventHandler</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

