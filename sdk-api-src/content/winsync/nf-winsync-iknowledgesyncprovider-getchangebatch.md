---
UID: NF:winsync.IKnowledgeSyncProvider.GetChangeBatch
title: IKnowledgeSyncProvider::GetChangeBatch (winsync.h)
description: Gets a change batch that contains item metadata for items that are not contained in the specified knowledge from the destination provider.
helpviewer_keywords: ["GetChangeBatch","GetChangeBatch method [Windows Sync]","GetChangeBatch method [Windows Sync]","IKnowledgeSyncProvider interface","IKnowledgeSyncProvider interface [Windows Sync]","GetChangeBatch method","IKnowledgeSyncProvider.GetChangeBatch","IKnowledgeSyncProvider::GetChangeBatch","winsync.iknowledgesyncprovider_getchangebatch","winsync/IKnowledgeSyncProvider::GetChangeBatch"]
old-location: winsync\iknowledgesyncprovider_getchangebatch.htm
tech.root: winsync
ms.assetid: 165eb8eb-092c-4084-a296-abc2421596d5
ms.date: 12/05/2018
ms.keywords: GetChangeBatch, GetChangeBatch method [Windows Sync], GetChangeBatch method [Windows Sync],IKnowledgeSyncProvider interface, IKnowledgeSyncProvider interface [Windows Sync],GetChangeBatch method, IKnowledgeSyncProvider.GetChangeBatch, IKnowledgeSyncProvider::GetChangeBatch, winsync.iknowledgesyncprovider_getchangebatch, winsync/IKnowledgeSyncProvider::GetChangeBatch
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
 - IKnowledgeSyncProvider::GetChangeBatch
 - winsync/IKnowledgeSyncProvider::GetChangeBatch
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
 - IKnowledgeSyncProvider.GetChangeBatch
---

# IKnowledgeSyncProvider::GetChangeBatch


## -description

Gets a change batch that contains item metadata for items that are not contained in the specified knowledge from the destination provider.

## -parameters

### -param dwBatchSize [in]

The requested number of changes to include in the change batch.

### -param pSyncKnowledge [in]

The knowledge from the destination provider. This knowledge must be mapped by calling  <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-mapremotetolocal">ISyncKnowledge::MapRemoteToLocal</a> on the source knowledge before it can be used for change enumeration.

### -param ppSyncChangeBatch [out]

Returns a change batch that contains item metadata for items that are not contained in <i>pSyncKnowledge</i>.

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

Be aware that <i>dwBatchSize</i> is a requested number only. A smaller or larger batch can be returned.


<div class="alert"><b>Note</b>  If there are no more changes to send after this batch, <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase::SetLastBatch</a> must be called on the returned change batch before <b>GetChangeBatch</b> is called again.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iknowledgesyncprovider">IKnowledgeSyncProvider Interface</a>