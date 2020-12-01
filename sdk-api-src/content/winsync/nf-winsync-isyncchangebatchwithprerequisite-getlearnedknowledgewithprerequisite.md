---
UID: NF:winsync.ISyncChangeBatchWithPrerequisite.GetLearnedKnowledgeWithPrerequisite
title: ISyncChangeBatchWithPrerequisite::GetLearnedKnowledgeWithPrerequisite (winsync.h)
description: Gets the knowledge that the destination replica learns when the destination provider applies all the changes in this change batch, based on the prerequisite knowledge of the change batch.
helpviewer_keywords: ["GetLearnedKnowledgeWithPrerequisite","GetLearnedKnowledgeWithPrerequisite method [Windows Sync]","GetLearnedKnowledgeWithPrerequisite method [Windows Sync]","ISyncChangeBatchWithPrerequisite interface","ISyncChangeBatchWithPrerequisite interface [Windows Sync]","GetLearnedKnowledgeWithPrerequisite method","ISyncChangeBatchWithPrerequisite.GetLearnedKnowledgeWithPrerequisite","ISyncChangeBatchWithPrerequisite::GetLearnedKnowledgeWithPrerequisite","winsync.isyncchangebatchwithprerequisite_getlearnedknowledgewithprerequisite","winsync/ISyncChangeBatchWithPrerequisite::GetLearnedKnowledgeWithPrerequisite"]
old-location: winsync\isyncchangebatchwithprerequisite_getlearnedknowledgewithprerequisite.htm
tech.root: winsync
ms.assetid: 691f2cc1-9acb-4474-b20a-31bb7810372e
ms.date: 12/05/2018
ms.keywords: GetLearnedKnowledgeWithPrerequisite, GetLearnedKnowledgeWithPrerequisite method [Windows Sync], GetLearnedKnowledgeWithPrerequisite method [Windows Sync],ISyncChangeBatchWithPrerequisite interface, ISyncChangeBatchWithPrerequisite interface [Windows Sync],GetLearnedKnowledgeWithPrerequisite method, ISyncChangeBatchWithPrerequisite.GetLearnedKnowledgeWithPrerequisite, ISyncChangeBatchWithPrerequisite::GetLearnedKnowledgeWithPrerequisite, winsync.isyncchangebatchwithprerequisite_getlearnedknowledgewithprerequisite, winsync/ISyncChangeBatchWithPrerequisite::GetLearnedKnowledgeWithPrerequisite
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
 - ISyncChangeBatchWithPrerequisite::GetLearnedKnowledgeWithPrerequisite
 - winsync/ISyncChangeBatchWithPrerequisite::GetLearnedKnowledgeWithPrerequisite
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
 - ISyncChangeBatchWithPrerequisite.GetLearnedKnowledgeWithPrerequisite
---

# ISyncChangeBatchWithPrerequisite::GetLearnedKnowledgeWithPrerequisite


## -description

Gets the knowledge that the destination replica learns when the destination provider applies all the changes in this change batch, based on the prerequisite knowledge of the change batch.

## -parameters

### -param pDestinationKnowledge [in]

A knowledge fragment is added to the returned learned knowledge only if <i>pDestinationKnowledge</i> contains the prerequisite knowledge for that fragment.

### -param ppLearnedWithPrerequisiteKnowledge [out]

The knowledge that the destination replica learns when the destination provider applies all the changes in this change batch, based on the prerequisite knowledge of the change batch.

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

The knowledge that is returned in <i>ppLearnedWithPrerequisiteKnowledge</i> is computed by calling the <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-projectontoknowledgewithprerequisite">ISyncKnowledge2::ProjectOntoKnowledgeWithPrerequisite</a> method of the learned knowledge of the change batch, passing <i>pDestinationKnowledge</i> as the template knowledge.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchwithprerequisite">ISyncChangeBatchWithPrerequisite Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge2">ISyncKnowledge2 Interface</a>