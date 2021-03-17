---
UID: NF:winsync.ISyncFullEnumerationChangeBatch.GetLearnedKnowledgeAfterRecoveryComplete
title: ISyncFullEnumerationChangeBatch::GetLearnedKnowledgeAfterRecoveryComplete (winsync.h)
description: Gets the knowledge the destination replica will learn after it applies all the changes in the recovery synchronization.
helpviewer_keywords: ["GetLearnedKnowledgeAfterRecoveryComplete","GetLearnedKnowledgeAfterRecoveryComplete method [Windows Sync]","GetLearnedKnowledgeAfterRecoveryComplete method [Windows Sync]","ISyncFullEnumerationChangeBatch interface","ISyncFullEnumerationChangeBatch interface [Windows Sync]","GetLearnedKnowledgeAfterRecoveryComplete method","ISyncFullEnumerationChangeBatch.GetLearnedKnowledgeAfterRecoveryComplete","ISyncFullEnumerationChangeBatch::GetLearnedKnowledgeAfterRecoveryComplete","winsync.isyncfullenumerationchangebatch_getlearnedknowledgeafterrecoverycomplete","winsync/ISyncFullEnumerationChangeBatch::GetLearnedKnowledgeAfterRecoveryComplete"]
old-location: winsync\isyncfullenumerationchangebatch_getlearnedknowledgeafterrecoverycomplete.htm
tech.root: winsync
ms.assetid: 8eb9fdbf-b1ce-4acf-837f-01d693940790
ms.date: 12/05/2018
ms.keywords: GetLearnedKnowledgeAfterRecoveryComplete, GetLearnedKnowledgeAfterRecoveryComplete method [Windows Sync], GetLearnedKnowledgeAfterRecoveryComplete method [Windows Sync],ISyncFullEnumerationChangeBatch interface, ISyncFullEnumerationChangeBatch interface [Windows Sync],GetLearnedKnowledgeAfterRecoveryComplete method, ISyncFullEnumerationChangeBatch.GetLearnedKnowledgeAfterRecoveryComplete, ISyncFullEnumerationChangeBatch::GetLearnedKnowledgeAfterRecoveryComplete, winsync.isyncfullenumerationchangebatch_getlearnedknowledgeafterrecoverycomplete, winsync/ISyncFullEnumerationChangeBatch::GetLearnedKnowledgeAfterRecoveryComplete
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
 - ISyncFullEnumerationChangeBatch::GetLearnedKnowledgeAfterRecoveryComplete
 - winsync/ISyncFullEnumerationChangeBatch::GetLearnedKnowledgeAfterRecoveryComplete
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
 - ISyncFullEnumerationChangeBatch.GetLearnedKnowledgeAfterRecoveryComplete
---

# ISyncFullEnumerationChangeBatch::GetLearnedKnowledgeAfterRecoveryComplete


## -description

Gets the knowledge the destination replica will learn after it applies all the changes in the recovery synchronization.

## -parameters

### -param ppLearnedKnowledgeAfterRecoveryComplete [out]

Returns the knowledge that the destination replica will learn after it applies all the changes in the recovery synchronization.

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
No group was added to the batch, or a group was opened but not ended.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfullenumerationchangebatch">ISyncFullEnumerationChangeBatch Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>