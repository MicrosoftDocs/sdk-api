---
UID: NF:winsync.ISyncChangeBatchBase.GetIsLastBatch
title: ISyncChangeBatchBase::GetIsLastBatch (winsync.h)
author: windows-sdk-content
description: Gets a flag that indicates whether the changes in this change batch are the last batch of a synchronization session.
old-location: winsync\isyncchangebatchbase_getislastbatch.htm
tech.root: winsync
ms.assetid: 74b82fde-c492-4d5f-a680-62b836420cee
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetIsLastBatch, GetIsLastBatch method [Windows Sync], GetIsLastBatch method [Windows Sync],ISyncChangeBatchBase interface, ISyncChangeBatchBase interface [Windows Sync],GetIsLastBatch method, ISyncChangeBatchBase.GetIsLastBatch, ISyncChangeBatchBase::GetIsLastBatch, winsync.isyncchangebatchbase_getislastbatch, winsync/ISyncChangeBatchBase::GetIsLastBatch
ms.topic: method
f1_keywords: ["winsync/ISyncChangeBatchBase.GetIsLastBatch"]
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
 - ISyncChangeBatchBase.GetIsLastBatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncChangeBatchBase::GetIsLastBatch


## -description


Gets a flag that indicates whether the changes in this change batch are the last batch of a synchronization session.


## -parameters




### -param pfLastBatch [out]

Returns a flag that indicates whether this batch is the last batch.


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
<dt><b>E_POINTER

</b></dt>
</dl>
</td>
<td width="60%">
<i>pfLastBatch</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



When returning a change batch in response to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-getchangebatch">IKnowledgeSyncProvider::GetChangeBatch</a> method, the source provider must call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-setlastbatch">SetLastBatch</a> if the change batch is the last batch of changes. 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>
 

 

