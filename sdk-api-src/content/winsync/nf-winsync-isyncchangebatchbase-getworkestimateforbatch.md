---
UID: NF:winsync.ISyncChangeBatchBase.GetWorkEstimateForBatch
title: ISyncChangeBatchBase::GetWorkEstimateForBatch (winsync.h)
description: Gets the work estimate for the batch.
helpviewer_keywords: ["GetWorkEstimateForBatch","GetWorkEstimateForBatch method [Windows Sync]","GetWorkEstimateForBatch method [Windows Sync]","ISyncChangeBatchBase interface","ISyncChangeBatchBase interface [Windows Sync]","GetWorkEstimateForBatch method","ISyncChangeBatchBase.GetWorkEstimateForBatch","ISyncChangeBatchBase::GetWorkEstimateForBatch","winsync.isyncchangebatchbase_getworkestimateforbatch","winsync/ISyncChangeBatchBase::GetWorkEstimateForBatch"]
old-location: winsync\isyncchangebatchbase_getworkestimateforbatch.htm
tech.root: winsync
ms.assetid: 4abf4027-814a-461d-b179-b2510abccc5e
ms.date: 12/05/2018
ms.keywords: GetWorkEstimateForBatch, GetWorkEstimateForBatch method [Windows Sync], GetWorkEstimateForBatch method [Windows Sync],ISyncChangeBatchBase interface, ISyncChangeBatchBase interface [Windows Sync],GetWorkEstimateForBatch method, ISyncChangeBatchBase.GetWorkEstimateForBatch, ISyncChangeBatchBase::GetWorkEstimateForBatch, winsync.isyncchangebatchbase_getworkestimateforbatch, winsync/ISyncChangeBatchBase::GetWorkEstimateForBatch
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
 - ISyncChangeBatchBase::GetWorkEstimateForBatch
 - winsync/ISyncChangeBatchBase::GetWorkEstimateForBatch
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
 - ISyncChangeBatchBase.GetWorkEstimateForBatch
---

# ISyncChangeBatchBase::GetWorkEstimateForBatch


## -description

Gets the work estimate for the batch.

## -parameters

### -param pdwWorkForBatch [out]

Returns the work estimate for the batch. The default value is 0.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>

## -remarks

The work estimate is determined by the provider and is typically understood as the total work for all changes in a single batch and as a portion of the total work estimated for the session.

This value is reported in the <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isynccallback-onprogress">OnProgress</a> event.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>