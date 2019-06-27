---
UID: NN:winsync.ISyncChange
title: ISyncChange (winsync.h)
author: windows-sdk-content
description: Represents a change to an item.
old-location: winsync\isyncchange.htm
tech.root: winsync
ms.assetid: 0cd29977-8d02-4a1e-b63f-783cc10021ee
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncChange, ISyncChange interface [Windows Sync], ISyncChange interface [Windows Sync],described, winsync.isyncchange, winsync/ISyncChange
ms.topic: interface
f1_keywords: 
 - "winsync/ISyncChange"
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
 - ISyncChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncChange interface


## -description


Represents a change to an item.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncChange</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncChange</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncChange</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchange-getchangeunits">GetChangeUnits</a>
</td>
<td align="left" width="63%">
Gets an object that can enumerate change units that are contained in this change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchange-getchangeversion">GetChangeVersion</a>
</td>
<td align="left" width="63%">
Gets the version that is associated with this change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchange-getcreationversion">GetCreationVersion</a>
</td>
<td align="left" width="63%">
Gets the creation version of the changed item.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchange-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Gets flags that are associated with this change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchange-getlearnedknowledge">GetLearnedKnowledge</a>
</td>
<td align="left" width="63%">
Gets the knowledge that a replica will learn when this change is applied to its item store.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchange-getmadewithknowledge">GetMadeWithKnowledge</a>
</td>
<td align="left" width="63%">
Gets the made-with knowledge for this change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchange-getownerreplicaid">GetOwnerReplicaId</a>
</td>
<td align="left" width="63%">
Gets the ID of the replica that originated this change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchange-getrootitemid">GetRootItemId</a>
</td>
<td align="left" width="63%">
Gets the ID of the changed item.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchange-getworkestimate">GetWorkEstimate</a>
</td>
<td align="left" width="63%">
Gets the work estimate for this change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchange-setworkestimate">SetWorkEstimate</a>
</td>
<td align="left" width="63%">
Sets the work estimate for this change.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

