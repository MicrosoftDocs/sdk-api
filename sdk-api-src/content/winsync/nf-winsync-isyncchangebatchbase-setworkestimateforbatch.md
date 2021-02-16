---
UID: NF:winsync.ISyncChangeBatchBase.SetWorkEstimateForBatch
title: ISyncChangeBatchBase::SetWorkEstimateForBatch (winsync.h)
description: Sets the work estimate for the batch.
helpviewer_keywords: ["ISyncChangeBatchBase interface [Windows Sync]","SetWorkEstimateForBatch method","ISyncChangeBatchBase.SetWorkEstimateForBatch","ISyncChangeBatchBase::SetWorkEstimateForBatch","SetWorkEstimateForBatch","SetWorkEstimateForBatch method [Windows Sync]","SetWorkEstimateForBatch method [Windows Sync]","ISyncChangeBatchBase interface","winsync.isyncchangebatchbase_setworkestimateforbatch","winsync/ISyncChangeBatchBase::SetWorkEstimateForBatch"]
old-location: winsync\isyncchangebatchbase_setworkestimateforbatch.htm
tech.root: winsync
ms.assetid: da88dd49-4b11-444c-8137-212f8c673122
ms.date: 12/05/2018
ms.keywords: ISyncChangeBatchBase interface [Windows Sync],SetWorkEstimateForBatch method, ISyncChangeBatchBase.SetWorkEstimateForBatch, ISyncChangeBatchBase::SetWorkEstimateForBatch, SetWorkEstimateForBatch, SetWorkEstimateForBatch method [Windows Sync], SetWorkEstimateForBatch method [Windows Sync],ISyncChangeBatchBase interface, winsync.isyncchangebatchbase_setworkestimateforbatch, winsync/ISyncChangeBatchBase::SetWorkEstimateForBatch
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
 - ISyncChangeBatchBase::SetWorkEstimateForBatch
 - winsync/ISyncChangeBatchBase::SetWorkEstimateForBatch
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
 - ISyncChangeBatchBase.SetWorkEstimateForBatch
---

# ISyncChangeBatchBase::SetWorkEstimateForBatch


## -description

Sets the work estimate for the batch.

## -parameters

### -param dwWorkForBatch [in]

The work estimate for the batch.

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

The work estimate is determined by the provider and typically is understood as the total work for all changes in a single batch and as a portion of the total work estimated for the session.

This value is reported in the <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isynccallback-onprogress">OnProgress</a> event.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isynccallback">ISyncCallback Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>