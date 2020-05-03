---
UID: NN:uianimation.IUIAnimationStoryboardEventHandler
title: IUIAnimationStoryboardEventHandler (uianimation.h)
description: Defines methods for handling status and update events for a storyboard.
helpviewer_keywords: ["IUIAnimationStoryboardEventHandler","IUIAnimationStoryboardEventHandler interface [Windows Animation]","IUIAnimationStoryboardEventHandler interface [Windows Animation]","described","uianimation.iuianimationstoryboardeventhandler","uianimation/IUIAnimationStoryboardEventHandler"]
old-location: uianimation\iuianimationstoryboardeventhandler.htm
tech.root: UIAnimation
ms.assetid: f43f53f9-1491-4847-89ef-e65ba98a2127
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboardEventHandler, IUIAnimationStoryboardEventHandler interface [Windows Animation], IUIAnimationStoryboardEventHandler interface [Windows Animation],described, uianimation.iuianimationstoryboardeventhandler, uianimation/IUIAnimationStoryboardEventHandler
f1_keywords:
- uianimation/IUIAnimationStoryboardEventHandler
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
- IUIAnimationStoryboardEventHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationStoryboardEventHandler interface


## -description


Defines methods for handling status and update events for a storyboard.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationStoryboardEventHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationStoryboardEventHandler</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler-onstoryboardstatuschanged">OnStoryboardStatusChanged</a>
</td>
<td align="left" width="63%">
Handles events that occur when a storyboard's status changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler-onstoryboardupdated">OnStoryboardUpdated</a>
</td>
<td align="left" width="63%">
Handles events that occur when a storyboard is updated.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-getstatus">IUIAnimationStoryboard::GetStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-setstoryboardeventhandler">IUIAnimationStoryboard::SetStoryboardEventHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_STATUS</a>
 

 

