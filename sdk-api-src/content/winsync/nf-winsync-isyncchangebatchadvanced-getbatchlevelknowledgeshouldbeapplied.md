---
UID: NF:winsync.ISyncChangeBatchAdvanced.GetBatchLevelKnowledgeShouldBeApplied
title: ISyncChangeBatchAdvanced::GetBatchLevelKnowledgeShouldBeApplied (winsync.h)
description: Gets a value that indicates whether the learned knowledge for the batch must be saved after the batch is applied to the destination replica.
helpviewer_keywords: ["GetBatchLevelKnowledgeShouldBeApplied","GetBatchLevelKnowledgeShouldBeApplied method [Windows Sync]","GetBatchLevelKnowledgeShouldBeApplied method [Windows Sync]","ISyncChangeBatchAdvanced interface","ISyncChangeBatchAdvanced interface [Windows Sync]","GetBatchLevelKnowledgeShouldBeApplied method","ISyncChangeBatchAdvanced.GetBatchLevelKnowledgeShouldBeApplied","ISyncChangeBatchAdvanced::GetBatchLevelKnowledgeShouldBeApplied","winsync.isyncchangebatchadvanced_getbatchlevelknowledgeshouldbeapplied","winsync/ISyncChangeBatchAdvanced::GetBatchLevelKnowledgeShouldBeApplied"]
old-location: winsync\isyncchangebatchadvanced_getbatchlevelknowledgeshouldbeapplied.htm
tech.root: winsync
ms.assetid: 911ac2dd-a8df-4f71-81da-032219664453
ms.date: 12/05/2018
ms.keywords: GetBatchLevelKnowledgeShouldBeApplied, GetBatchLevelKnowledgeShouldBeApplied method [Windows Sync], GetBatchLevelKnowledgeShouldBeApplied method [Windows Sync],ISyncChangeBatchAdvanced interface, ISyncChangeBatchAdvanced interface [Windows Sync],GetBatchLevelKnowledgeShouldBeApplied method, ISyncChangeBatchAdvanced.GetBatchLevelKnowledgeShouldBeApplied, ISyncChangeBatchAdvanced::GetBatchLevelKnowledgeShouldBeApplied, winsync.isyncchangebatchadvanced_getbatchlevelknowledgeshouldbeapplied, winsync/ISyncChangeBatchAdvanced::GetBatchLevelKnowledgeShouldBeApplied
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
 - ISyncChangeBatchAdvanced::GetBatchLevelKnowledgeShouldBeApplied
 - winsync/ISyncChangeBatchAdvanced::GetBatchLevelKnowledgeShouldBeApplied
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
 - ISyncChangeBatchAdvanced.GetBatchLevelKnowledgeShouldBeApplied
---

# ISyncChangeBatchAdvanced::GetBatchLevelKnowledgeShouldBeApplied


## -description

Gets a value that indicates whether the learned knowledge for the batch must be saved after the batch is applied to the destination replica.

## -parameters

### -param pfBatchKnowledgeShouldBeApplied [out]

Returns a value that indicates whether the learned knowledge for the batch must be saved after the batch is applied to the destination replica.

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
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_BATCH_NEEDS_KNOWLEDGE</b></dt>
</dl>
</td>
<td width="60%">
The change batch contains no changes and no knowledge.

</td>
</tr>
</table>

## -remarks

Typically, the destination provider saves the learned knowledge for each item change as it is applied to the destination replica. The value that is returned by <b>GetBatchLevelKnowledgeShouldBeApplied</b> indicates whether it is also necessary to save the learned knowledge of the change batch after the entire change batch has been applied. The learned knowledge of the change batch can be obtained by calling <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-getlearnedknowledge">ISyncChangeBatchBase::GetLearnedKnowledge</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchadvanced">ISyncChangeBatchAdvanced Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>