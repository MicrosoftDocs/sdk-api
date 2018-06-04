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

# IFeedClockVectorElement interface


## -description


Represents a clock vector element that contains FeedSync information.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFeedClockVectorElement</b> interface inherits from <b>IClockVectorElement</b>. <b>IFeedClockVectorElement</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFeedClockVectorElement</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546791">GetFlags</a>
</td>
<td align="left" width="63%">
Gets flags that specify additional information about the clock vector element.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f39b3bdf-a37e-4673-a620-5b14109718cb">GetSyncTime</a>
</td>
<td align="left" width="63%">
Gets a <a href="https://msdn.microsoft.com/f5e0df02-d016-4eae-9b9b-bfd754ade126">SYNC_TIME</a> value that corresponds to the <b>when</b> value for the item.


</td>
</tr>
</table> 


## -see-also




<b>IClockVectorElement</b>



<a href="https://msdn.microsoft.com/f5e0df02-d016-4eae-9b9b-bfd754ade126">SYNC_TIME Structure</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

