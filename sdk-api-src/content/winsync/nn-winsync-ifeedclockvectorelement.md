---
UID: NN:winsync.IFeedClockVectorElement
title: IFeedClockVectorElement
author: windows-sdk-content
description: Represents a clock vector element that contains FeedSync information.
old-location: winsync\ifeedclockvectorelement.htm
old-project: winsync
ms.assetid: 7ffc228f-c4f2-4451-9b23-ec78bf6c8318
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IFeedClockVectorElement, IFeedClockVectorElement interface [Windows Sync], IFeedClockVectorElement interface [Windows Sync],described, winsync.ifeedclockvectorelement, winsync/IFeedClockVectorElement
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	IFeedClockVectorElement
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

