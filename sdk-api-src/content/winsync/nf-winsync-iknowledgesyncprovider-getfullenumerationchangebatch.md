---
UID: NF:winsync.IKnowledgeSyncProvider.GetFullEnumerationChangeBatch
title: IKnowledgeSyncProvider::GetFullEnumerationChangeBatch (winsync.h)
description: Gets a change batch that contains item metadata for items that have IDs greater than the specified lower bound, as part of a full enumeration.
helpviewer_keywords: ["GetFullEnumerationChangeBatch","GetFullEnumerationChangeBatch method [Windows Sync]","GetFullEnumerationChangeBatch method [Windows Sync]","IKnowledgeSyncProvider interface","IKnowledgeSyncProvider interface [Windows Sync]","GetFullEnumerationChangeBatch method","IKnowledgeSyncProvider.GetFullEnumerationChangeBatch","IKnowledgeSyncProvider::GetFullEnumerationChangeBatch","winsync.iknowledgesyncprovider_getfullenumerationchangebatch","winsync/IKnowledgeSyncProvider::GetFullEnumerationChangeBatch"]
old-location: winsync\iknowledgesyncprovider_getfullenumerationchangebatch.htm
tech.root: winsync
ms.assetid: 344d0921-1e4e-4813-a095-8ae9ddf734f1
ms.date: 12/05/2018
ms.keywords: GetFullEnumerationChangeBatch, GetFullEnumerationChangeBatch method [Windows Sync], GetFullEnumerationChangeBatch method [Windows Sync],IKnowledgeSyncProvider interface, IKnowledgeSyncProvider interface [Windows Sync],GetFullEnumerationChangeBatch method, IKnowledgeSyncProvider.GetFullEnumerationChangeBatch, IKnowledgeSyncProvider::GetFullEnumerationChangeBatch, winsync.iknowledgesyncprovider_getfullenumerationchangebatch, winsync/IKnowledgeSyncProvider::GetFullEnumerationChangeBatch
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKnowledgeSyncProvider::GetFullEnumerationChangeBatch
 - winsync/IKnowledgeSyncProvider::GetFullEnumerationChangeBatch
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IKnowledgeSyncProvider.GetFullEnumerationChangeBatch
---

# IKnowledgeSyncProvider::GetFullEnumerationChangeBatch


## -description

Gets a change batch that contains item metadata for items that have IDs greater than the specified lower bound, as part of a full enumeration.

## -parameters

### -param dwBatchSize [in]

The number of changes to include in the change batch.

### -param pbLowerEnumerationBound [in]

The lower bound for item IDs. This method returns changes that have IDs greater than or equal to this ID value.

### -param pSyncKnowledge [in]

If an item change is contained in this knowledge object, data for that item already exists on the destination replica.

### -param ppSyncChangeBatch [out]

Returns a change batch that contains item metadata for items that have IDs greater than the specified lower bound.

### -param ppUnkDataRetriever [out]

Returns an object that can be used to retrieve change data. It can be an <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isynchronousdataretriever">ISynchronousDataRetriever</a> object or a provider-specific object.

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Provider-determined error codes</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -remarks

This method enumerates, in sorted order by item ID, changes that have an item ID of <i>pbLowerEnumerationBound</i> or greater. This enables a synchronization session to determine which items on the destination provider have been deleted but forgotten by the source provider. Optionally, this method can also add changes to the batch, sorted by item ID, that have item ID less than <i>pbLowerEnumerationBound</i> and that are not contained in the destination knowledge.

<div class="alert"><b>Note</b>  If there are no more changes to send after this batch, <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-setlastbatch">ISyncChangeBatchBase::SetLastBatch</a> must be called on the returned change batch. Otherwise, the synchronization session calls <b>GetFullEnumerationChangeBatch</b> again to retrieve another batch of changes.<p class="note">For a provider that sends item data together with item change metadata, <i>pSyncKnowledge</i> can be used to determine whether it is necessary to send item data. Item data does not have to be sent when the item change is contained in <i>pSyncKnowledge</i>. Be aware that before it can be used to check items for containment, <i>pSyncKnowledge</i> must be mapped by using the <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-mapremotetolocal">ISyncKnowledge::MapRemoteToLocal</a> method on the knowledge object that is contained in the current provider.

</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iknowledgesyncprovider">IKnowledgeSyncProvider Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isynchronousdataretriever">ISynchronousDataRetriever Interface</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-reference">Windows Sync Reference</a>