---
UID: NF:winsync.ISyncChangeBatchWithPrerequisite.SetPrerequisiteKnowledge
title: ISyncChangeBatchWithPrerequisite::SetPrerequisiteKnowledge (winsync.h)
description: Sets the minimum knowledge that a destination provider is required to have to process this change batch.
helpviewer_keywords: ["ISyncChangeBatchWithPrerequisite interface [Windows Sync]","SetPrerequisiteKnowledge method","ISyncChangeBatchWithPrerequisite.SetPrerequisiteKnowledge","ISyncChangeBatchWithPrerequisite::SetPrerequisiteKnowledge","SetPrerequisiteKnowledge","SetPrerequisiteKnowledge method [Windows Sync]","SetPrerequisiteKnowledge method [Windows Sync]","ISyncChangeBatchWithPrerequisite interface","winsync.isyncchangebatchwithprerequisite_setprerequisiteknowledge","winsync/ISyncChangeBatchWithPrerequisite::SetPrerequisiteKnowledge"]
old-location: winsync\isyncchangebatchwithprerequisite_setprerequisiteknowledge.htm
tech.root: winsync
ms.assetid: a138dbd9-e498-40bf-9490-690103afbf0f
ms.date: 12/05/2018
ms.keywords: ISyncChangeBatchWithPrerequisite interface [Windows Sync],SetPrerequisiteKnowledge method, ISyncChangeBatchWithPrerequisite.SetPrerequisiteKnowledge, ISyncChangeBatchWithPrerequisite::SetPrerequisiteKnowledge, SetPrerequisiteKnowledge, SetPrerequisiteKnowledge method [Windows Sync], SetPrerequisiteKnowledge method [Windows Sync],ISyncChangeBatchWithPrerequisite interface, winsync.isyncchangebatchwithprerequisite_setprerequisiteknowledge, winsync/ISyncChangeBatchWithPrerequisite::SetPrerequisiteKnowledge
f1_keywords:
- winsync/ISyncChangeBatchWithPrerequisite.SetPrerequisiteKnowledge
dev_langs:
- c++
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
- ISyncChangeBatchWithPrerequisite.SetPrerequisiteKnowledge
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncChangeBatchWithPrerequisite::SetPrerequisiteKnowledge


## -description


Sets the minimum knowledge that a destination provider is required to have to process this change batch.


## -parameters




### -param pPrerequisiteKnowledge [in]

The minimum knowledge that a destination provider is required to have to process this change batch.


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
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchwithprerequisite">ISyncChangeBatchWithPrerequisite Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>
 

 

