---
UID: NF:winsync.ISyncChangeBatchBase.GetLearnedKnowledge
title: ISyncChangeBatchBase::GetLearnedKnowledge (winsync.h)
description: Gets the knowledge that the destination replica learns when the destination provider applies all the changes in this change batch.
helpviewer_keywords: ["GetLearnedKnowledge","GetLearnedKnowledge method [Windows Sync]","GetLearnedKnowledge method [Windows Sync]","ISyncChangeBatchBase interface","ISyncChangeBatchBase interface [Windows Sync]","GetLearnedKnowledge method","ISyncChangeBatchBase.GetLearnedKnowledge","ISyncChangeBatchBase::GetLearnedKnowledge","winsync.isyncchangebatchbase_getlearnedknowledge","winsync/ISyncChangeBatchBase::GetLearnedKnowledge"]
old-location: winsync\isyncchangebatchbase_getlearnedknowledge.htm
tech.root: winsync
ms.assetid: cef04646-71a7-489d-9beb-fe87bb949218
ms.date: 12/05/2018
ms.keywords: GetLearnedKnowledge, GetLearnedKnowledge method [Windows Sync], GetLearnedKnowledge method [Windows Sync],ISyncChangeBatchBase interface, ISyncChangeBatchBase interface [Windows Sync],GetLearnedKnowledge method, ISyncChangeBatchBase.GetLearnedKnowledge, ISyncChangeBatchBase::GetLearnedKnowledge, winsync.isyncchangebatchbase_getlearnedknowledge, winsync/ISyncChangeBatchBase::GetLearnedKnowledge
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
 - ISyncChangeBatchBase::GetLearnedKnowledge
 - winsync/ISyncChangeBatchBase::GetLearnedKnowledge
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
 - ISyncChangeBatchBase.GetLearnedKnowledge
---

# ISyncChangeBatchBase::GetLearnedKnowledge


## -description

Gets the knowledge that the destination replica learns when the destination provider applies all the changes in this change batch.

## -parameters

### -param ppLearnedKnowledge [out]

Returns the knowledge that a replica will learn when a provider applies all the changes in this change batch to the replica. This knowledge is valid only when the current knowledge of the replica contains the prerequisite knowledge of the change batch. The prerequisite knowledge can be obtained by calling <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-getprerequisiteknowledge">ISyncChangeBatchBase::GetPrerequisiteKnowledge</a>.

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
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The last group added to the batch was not ended.

</td>
</tr>
</table>

## -remarks

<b>GetLearnedKnowledge</b> can be used by a provider that uses a custom change applier.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>