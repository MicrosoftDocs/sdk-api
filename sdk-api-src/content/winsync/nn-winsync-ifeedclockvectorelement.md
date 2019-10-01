---
UID: NN:winsync.IFeedClockVectorElement
title: IFeedClockVectorElement (winsync.h)
author: windows-sdk-content
description: Represents a clock vector element that contains FeedSync information.
old-location: winsync\ifeedclockvectorelement.htm
tech.root: winsync
ms.assetid: 7ffc228f-c4f2-4451-9b23-ec78bf6c8318
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFeedClockVectorElement, IFeedClockVectorElement interface [Windows Sync], IFeedClockVectorElement interface [Windows Sync],described, winsync.ifeedclockvectorelement, winsync/IFeedClockVectorElement
ms.topic: interface
f1_keywords:
- winsync/IFeedClockVectorElement
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- winsync.h
api_name:
- IFeedClockVectorElement
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ifeedclockvectorelement-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Gets flags that specify additional information about the clock vector element.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ifeedclockvectorelement-getsynctime">GetSyncTime</a>
</td>
<td align="left" width="63%">
Gets a <a href="https://docs.microsoft.com/windows/desktop/api/winsync/ns-winsync-sync_time">SYNC_TIME</a> value that corresponds to the <b>when</b> value for the item.


</td>
</tr>
</table> 


## -see-also




<b>IClockVectorElement</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winsync/ns-winsync-sync_time">SYNC_TIME Structure</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

