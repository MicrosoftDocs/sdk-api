---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

