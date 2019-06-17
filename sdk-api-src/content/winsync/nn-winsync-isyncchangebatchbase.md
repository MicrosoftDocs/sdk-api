---
UID: NN:winsync.ISyncChangeBatchBase
title: ISyncChangeBatchBase (winsync.h)
author: windows-sdk-content
description: Represents metadata for a set of changes.
old-location: winsync\isyncchangebatchbase.htm
tech.root: winsync
ms.assetid: 14ca01a1-04eb-4282-adf0-e775d6ff0801
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncChangeBatchBase, ISyncChangeBatchBase interface [Windows Sync], ISyncChangeBatchBase interface [Windows Sync],described, winsync.isyncchangebatchbase, winsync/ISyncChangeBatchBase
ms.topic: interface
f1_keywords: ["winsync/ISyncChangeBatchBase"]
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
 - ISyncChangeBatchBase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncChangeBatchBase interface


## -description


Represents metadata for a set of changes.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncChangeBatchBase</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncChangeBatchBase</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncChangeBatchBase</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-additemmetadatatogroup">AddItemMetadataToGroup</a>
</td>
<td align="left" width="63%">
Adds a specified item change to the group that is currently open.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-beginorderedgroup">BeginOrderedGroup</a>
</td>
<td align="left" width="63%">
Opens an ordered group in the change batch. This group is ordered by item ID.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-endorderedgroup">EndOrderedGroup</a>
</td>
<td align="left" width="63%">
Closes a previously opened ordered group in the change batch.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-getchangeenumerator">GetChangeEnumerator</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-ienumsyncchanges">IEnumSyncChanges</a> object that enumerates the item changes in this change batch.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-getislastbatch">GetIsLastBatch</a>
</td>
<td align="left" width="63%">
Gets a flag that indicates whether the changes in this change batch are the last batch of a synchronization session.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-getlearnedknowledge">GetLearnedKnowledge</a>
</td>
<td align="left" width="63%">
Gets the knowledge that the destination replica learns when the destination provider applies the changes in this change batch.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-getprerequisiteknowledge">GetPrerequisiteKnowledge</a>
</td>
<td align="left" width="63%">
Gets the minimum knowledge that a destination provider is required to have to process this change batch.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-getremainingworkestimateforsession">GetRemainingWorkEstimateForSession</a>
</td>
<td align="left" width="63%">
Gets the estimate of the remaining work for the session.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-getsourceforgottenknowledge">GetSourceForgottenKnowledge</a>
</td>
<td align="left" width="63%">
Gets the forgotten knowledge of the source replica.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-getworkestimateforbatch">GetWorkEstimateForBatch</a>
</td>
<td align="left" width="63%">
Gets the work estimate for the batch.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-serialize">Serialize</a>
</td>
<td align="left" width="63%">
Serializes the change batch to an array of bytes.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-setlastbatch">SetLastBatch</a>
</td>
<td align="left" width="63%">
Sets a flag that indicates there are no more changes to be enumerated in the synchronization session.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-setremainingworkestimateforsession">SetRemainingWorkEstimateForSession</a>
</td>
<td align="left" width="63%">
Sets the estimate of the remaining work for the batch.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-setworkestimateforbatch">SetWorkEstimateForBatch</a>
</td>
<td align="left" width="63%">
Sets the work estimate for the session.


</td>
</tr>
</table> 


## -remarks



<b>ISyncChangeBatchBase</b> is the base interface for change batches. Typically, it is overridden by a derived interface, such as <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch</a> for a knowledge synchronization, and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfullenumerationchangebatch">ISyncFullEnumerationChangeBatch</a> for a full enumeration synchronization.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-ienumsyncchanges">IEnumSyncChanges Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchadvanced">ISyncChangeBatchAdvanced Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase2">ISyncChangeBatchBase2 Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchwithprerequisite">ISyncChangeBatchWithPrerequisite Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfullenumerationchangebatch">ISyncFullEnumerationChangeBatch Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

