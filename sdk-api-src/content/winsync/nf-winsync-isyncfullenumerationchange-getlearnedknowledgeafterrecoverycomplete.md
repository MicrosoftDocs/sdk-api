---
UID: NF:winsync.ISyncFullEnumerationChange.GetLearnedKnowledgeAfterRecoveryComplete
title: ISyncFullEnumerationChange::GetLearnedKnowledgeAfterRecoveryComplete (winsync.h)
description: Gets the knowledge the destination replica will learn after it applies the changes in the full enumeration.
helpviewer_keywords: ["GetLearnedKnowledgeAfterRecoveryComplete","GetLearnedKnowledgeAfterRecoveryComplete method [Windows Sync]","GetLearnedKnowledgeAfterRecoveryComplete method [Windows Sync]","ISyncFullEnumerationChange interface","ISyncFullEnumerationChange interface [Windows Sync]","GetLearnedKnowledgeAfterRecoveryComplete method","ISyncFullEnumerationChange.GetLearnedKnowledgeAfterRecoveryComplete","ISyncFullEnumerationChange::GetLearnedKnowledgeAfterRecoveryComplete","winsync.isyncfullenumerationchange_getlearnedknowledgeafterrecoverycomplete","winsync/ISyncFullEnumerationChange::GetLearnedKnowledgeAfterRecoveryComplete"]
old-location: winsync\isyncfullenumerationchange_getlearnedknowledgeafterrecoverycomplete.htm
tech.root: winsync
ms.assetid: b6d536ad-557a-489d-a3e3-a4ffd69be096
ms.date: 12/05/2018
ms.keywords: GetLearnedKnowledgeAfterRecoveryComplete, GetLearnedKnowledgeAfterRecoveryComplete method [Windows Sync], GetLearnedKnowledgeAfterRecoveryComplete method [Windows Sync],ISyncFullEnumerationChange interface, ISyncFullEnumerationChange interface [Windows Sync],GetLearnedKnowledgeAfterRecoveryComplete method, ISyncFullEnumerationChange.GetLearnedKnowledgeAfterRecoveryComplete, ISyncFullEnumerationChange::GetLearnedKnowledgeAfterRecoveryComplete, winsync.isyncfullenumerationchange_getlearnedknowledgeafterrecoverycomplete, winsync/ISyncFullEnumerationChange::GetLearnedKnowledgeAfterRecoveryComplete
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
 - ISyncFullEnumerationChange::GetLearnedKnowledgeAfterRecoveryComplete
 - winsync/ISyncFullEnumerationChange::GetLearnedKnowledgeAfterRecoveryComplete
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
 - ISyncFullEnumerationChange.GetLearnedKnowledgeAfterRecoveryComplete
---

# ISyncFullEnumerationChange::GetLearnedKnowledgeAfterRecoveryComplete


## -description

Gets the knowledge the destination replica will learn after it applies the changes in the full enumeration.

## -parameters

### -param ppLearnedKnowledge [out]

The knowledge that the destination replica will learn after it applies this change during recovery synchronization.

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
<dt><b>SYNC_E_CHANGE_NEEDS_KNOWLEDGE</b></dt>
</dl>
</td>
<td width="60%">
This change does not contain made-with knowledge.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
Recovery synchronization is not in process.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfullenumerationchange">ISyncFullEnumerationChange</a>