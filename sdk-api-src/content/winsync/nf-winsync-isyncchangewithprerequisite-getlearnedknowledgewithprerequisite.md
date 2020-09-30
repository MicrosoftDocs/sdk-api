---
UID: NF:winsync.ISyncChangeWithPrerequisite.GetLearnedKnowledgeWithPrerequisite
title: ISyncChangeWithPrerequisite::GetLearnedKnowledgeWithPrerequisite (winsync.h)
description: Gets the knowledge that the destination replica learns when the destination provider applies this change, based on the prerequisite knowledge that is associated with the change.
helpviewer_keywords: ["GetLearnedKnowledgeWithPrerequisite","GetLearnedKnowledgeWithPrerequisite method [Windows Sync]","GetLearnedKnowledgeWithPrerequisite method [Windows Sync]","ISyncChangeWithPrerequisite interface","ISyncChangeWithPrerequisite interface [Windows Sync]","GetLearnedKnowledgeWithPrerequisite method","ISyncChangeWithPrerequisite.GetLearnedKnowledgeWithPrerequisite","ISyncChangeWithPrerequisite::GetLearnedKnowledgeWithPrerequisite","winsync.isyncchangewithprerequisite_getlearnedknowledgewithprerequisite","winsync/ISyncChangeWithPrerequisite::GetLearnedKnowledgeWithPrerequisite"]
old-location: winsync\isyncchangewithprerequisite_getlearnedknowledgewithprerequisite.htm
tech.root: winsync
ms.assetid: 5717f126-9383-4304-88eb-1d0fa3bb762f
ms.date: 12/05/2018
ms.keywords: GetLearnedKnowledgeWithPrerequisite, GetLearnedKnowledgeWithPrerequisite method [Windows Sync], GetLearnedKnowledgeWithPrerequisite method [Windows Sync],ISyncChangeWithPrerequisite interface, ISyncChangeWithPrerequisite interface [Windows Sync],GetLearnedKnowledgeWithPrerequisite method, ISyncChangeWithPrerequisite.GetLearnedKnowledgeWithPrerequisite, ISyncChangeWithPrerequisite::GetLearnedKnowledgeWithPrerequisite, winsync.isyncchangewithprerequisite_getlearnedknowledgewithprerequisite, winsync/ISyncChangeWithPrerequisite::GetLearnedKnowledgeWithPrerequisite
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ISyncChangeWithPrerequisite::GetLearnedKnowledgeWithPrerequisite
 - winsync/ISyncChangeWithPrerequisite::GetLearnedKnowledgeWithPrerequisite
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
 - ISyncChangeWithPrerequisite.GetLearnedKnowledgeWithPrerequisite
---

# ISyncChangeWithPrerequisite::GetLearnedKnowledgeWithPrerequisite


## -description

Gets the knowledge that the destination replica learns when the destination provider applies this change, based on the prerequisite knowledge that is associated with the change.

## -parameters

### -param pDestinationKnowledge [in]

The knowledge of a change unit that is contained in this change is not added to the returned learned knowledge when <i>pDestinationKnowledge</i> contains the prerequisite knowledge for the change unit.

### -param ppLearnedKnowledgeWithPrerequisite [out]

The knowledge that the destination replica learns when the destination provider applies this change, based on the prerequisite knowledge that is associated with the change.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory available to return the knowledge.

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
This object does not contain prerequisite knowledge.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangewithprerequisite">ISyncChangeWithPrerequisite Interface</a>