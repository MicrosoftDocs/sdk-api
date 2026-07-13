---
UID: NF:winsync.ISyncChangeBatchBase.SetLastBatch
title: ISyncChangeBatchBase::SetLastBatch (winsync.h)
description: Sets a flag that indicates there are no more changes to be enumerated in the synchronization session.
helpviewer_keywords: ["ISyncChangeBatchBase interface [Windows Sync]","SetLastBatch method","ISyncChangeBatchBase.SetLastBatch","ISyncChangeBatchBase::SetLastBatch","SetLastBatch","SetLastBatch method [Windows Sync]","SetLastBatch method [Windows Sync]","ISyncChangeBatchBase interface","winsync.isyncchangebatchbase_setlastbatch","winsync/ISyncChangeBatchBase::SetLastBatch"]
old-location: winsync\isyncchangebatchbase_setlastbatch.htm
tech.root: winsync
ms.assetid: 7619b446-5c71-4533-8af6-15f06dda3c87
ms.date: 12/05/2018
ms.keywords: ISyncChangeBatchBase interface [Windows Sync],SetLastBatch method, ISyncChangeBatchBase.SetLastBatch, ISyncChangeBatchBase::SetLastBatch, SetLastBatch, SetLastBatch method [Windows Sync], SetLastBatch method [Windows Sync],ISyncChangeBatchBase interface, winsync.isyncchangebatchbase_setlastbatch, winsync/ISyncChangeBatchBase::SetLastBatch
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
 - ISyncChangeBatchBase::SetLastBatch
 - winsync/ISyncChangeBatchBase::SetLastBatch
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
 - ISyncChangeBatchBase.SetLastBatch
---

# ISyncChangeBatchBase::SetLastBatch


## -description

Sets a flag that indicates there are no more changes to be enumerated in the synchronization session.



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
</table>

## -remarks

When returning a change batch in response to the <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-getchangebatch">IKnowledgeSyncProvider::GetChangeBatch</a> method, the source provider must call <b>SetLastBatch</b> if the change batch is the last batch of changes.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iknowledgesyncprovider">IKnowledgeSyncProvider Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>
