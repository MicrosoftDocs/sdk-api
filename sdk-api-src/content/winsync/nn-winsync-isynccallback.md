---
UID: NN:winsync.ISyncCallback
title: ISyncCallback (winsync.h)
author: windows-sdk-content
description: Represents application callbacks that are used to notify the application of synchronization events.
old-location: winsync\isynccallback.htm
tech.root: winsync
ms.assetid: f6c96e02-e9db-402c-8197-580f688b068f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncCallback, ISyncCallback interface [Windows Sync], ISyncCallback interface [Windows Sync],described, winsync.isynccallback, winsync/ISyncCallback
ms.topic: interface
f1_keywords: ["winsync/ISyncCallback"]
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
 - ISyncCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncCallback interface


## -description


Represents application callbacks that are used to notify the application of synchronization events.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isynccallback-onchange">OnChange</a>
</td>
<td align="left" width="63%">
Occurs before a change is applied.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isynccallback-onconflict">OnConflict</a>
</td>
<td align="left" width="63%">
Occurs when a conflict is detected when the concurrency conflict resolution policy is set to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/ne-winsync-__midl___midl_itf_winsync_0000_0000_0002">CRP_NONE</a>.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isynccallback-onfullenumerationneeded">OnFullEnumerationNeeded</a>
</td>
<td align="left" width="63%">
Occurs when the forgotten knowledge from the source provider is not contained in the current knowledge of the destination provider.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isynccallback-onprogress">OnProgress</a>
</td>
<td align="left" width="63%">
Occurs periodically during the synchronization session to report progress.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isynccallback-onrecoverableerror">OnRecoverableError</a>
</td>
<td align="left" width="63%">
Occurs when a synchronization provider sets a recoverable error while it is loading or saving an item.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/ne-winsync-__midl___midl_itf_winsync_0000_0000_0002">CONFLICT_RESOLUTION_POLICY Enumeration</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-reference">Windows Sync Reference</a>
 

 

