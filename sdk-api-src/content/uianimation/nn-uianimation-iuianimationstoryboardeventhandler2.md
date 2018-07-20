---
UID: NN:uianimation.IUIAnimationStoryboardEventHandler2
title: IUIAnimationStoryboardEventHandler2
author: windows-sdk-content
description: Defines methods for handling storyboard events.
old-location: uianimation\iuianimationstoryboardeventhandler2.htm
old-project: UIAnimation
ms.assetid: 2AB8C0C5-2203-4778-BBEA-6D52B727FDDB
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IUIAnimationStoryboardEventHandler2, IUIAnimationStoryboardEventHandler2 interface [Windows Animation], IUIAnimationStoryboardEventHandler2 interface [Windows Animation],described, uianimation.iuianimationstoryboardeventhandler2, uianimation/IUIAnimationStoryboardEventHandler2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IUIAnimationStoryboardEventHandler2
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboardEventHandler2 interface


## -description


Defines methods for handling storyboard events. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationStoryboardEventHandler2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationStoryboardEventHandler2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6C428A75-755D-4171-A714-83FC65A9D972">OnStoryboardStatusChanged</a>
</td>
<td align="left" width="63%">

      Handles storyboard status change events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30AB185A-D555-47CA-A2E6-DAAEB0C56FCD">OnStoryboardUpdated</a>
</td>
<td align="left" width="63%">
Handles storyboard update events.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1694B720-891A-4214-A009-6AA722E5B83D">
      IUIAnimationStoryboard2::GetStatus</a>



<a href="https://msdn.microsoft.com/9C105DDC-4BED-45FC-B4AE-2331A228BB86">IUIAnimationStoryboard2::SetStoryboardEventHandler</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/02830092-0070-44dc-8db2-239941134473">
      UI_ANIMATION_STORYBOARD_STATUS</a>
 

 

