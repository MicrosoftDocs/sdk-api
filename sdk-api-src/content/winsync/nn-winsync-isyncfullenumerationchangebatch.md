---
UID: NN:winsync.ISyncFullEnumerationChangeBatch
title: ISyncFullEnumerationChangeBatch (winsync.h)
author: windows-sdk-content
description: Represents the metadata for a set of changes that is created as part of a recovery synchronization.
old-location: winsync\isyncfullenumerationchangebatch.htm
tech.root: winsync
ms.assetid: 9086991d-03e3-4f2c-ad03-c1f554fe32ce
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncFullEnumerationChangeBatch, ISyncFullEnumerationChangeBatch interface [Windows Sync], ISyncFullEnumerationChangeBatch interface [Windows Sync],described, winsync.isyncfullenumerationchangebatch, winsync/ISyncFullEnumerationChangeBatch
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
 - ISyncFullEnumerationChangeBatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncFullEnumerationChangeBatch interface


## -description


Represents the metadata for a set of changes that is created as part of a recovery synchronization.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncFullEnumerationChangeBatch</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase</a>. <b>ISyncFullEnumerationChangeBatch</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncFullEnumerationChangeBatch</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncfullenumerationchangebatch-getclosedlowerbounditemid">GetClosedLowerBoundItemId</a>
</td>
<td align="left" width="63%">
Gets the closed lower bound on item IDs that require destination versions.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncfullenumerationchangebatch-getclosedupperbounditemid">GetClosedUpperBoundItemId</a>
</td>
<td align="left" width="63%">
Gets the closed upper bound on item IDs that require destination versions.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncfullenumerationchangebatch-getlearnedknowledgeafterrecoverycomplete">GetLearnedKnowledgeAfterRecoveryComplete</a>
</td>
<td align="left" width="63%">
Gets the knowledge the destination replica will learn after it applies all the changes in the recovery synchronization.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

