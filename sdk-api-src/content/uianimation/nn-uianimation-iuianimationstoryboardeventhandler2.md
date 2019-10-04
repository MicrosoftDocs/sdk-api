---
UID: NN:uianimation.IUIAnimationStoryboardEventHandler2
title: IUIAnimationStoryboardEventHandler2 (uianimation.h)
author: windows-sdk-content
description: Defines methods for handling storyboard events.
old-location: uianimation\iuianimationstoryboardeventhandler2.htm
tech.root: UIAnimation
ms.assetid: 2AB8C0C5-2203-4778-BBEA-6D52B727FDDB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboardEventHandler2, IUIAnimationStoryboardEventHandler2 interface [Windows Animation], IUIAnimationStoryboardEventHandler2 interface [Windows Animation],described, uianimation.iuianimationstoryboardeventhandler2, uianimation/IUIAnimationStoryboardEventHandler2
ms.topic: interface
f1_keywords: 
 - "uianimation/IUIAnimationStoryboardEventHandler2"
dev_langs:
 - c++
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps \| UWP apps]
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
 - IUIAnimationStoryboardEventHandler2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationStoryboardEventHandler2 interface


## -description


Defines methods for handling storyboard events. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationStoryboardEventHandler2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationStoryboardEventHandler2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationStoryboardEventHandler2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler2-onstoryboardstatuschanged">OnStoryboardStatusChanged</a>
</td>
<td align="left" width="63%">
Handles storyboard status change events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboardeventhandler2-onstoryboardupdated">OnStoryboardUpdated</a>
</td>
<td align="left" width="63%">
Handles storyboard update events.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-getstatus">IUIAnimationStoryboard2::GetStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-setstoryboardeventhandler">IUIAnimationStoryboard2::SetStoryboardEventHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_STATUS</a>
 

 

