---
UID: NF:winsync.ISyncChangeWithPrerequisite.GetPrerequisiteKnowledge
title: ISyncChangeWithPrerequisite::GetPrerequisiteKnowledge (winsync.h)
description: Gets the minimum knowledge that a destination provider is required to have to process this change.
helpviewer_keywords: ["GetPrerequisiteKnowledge","GetPrerequisiteKnowledge method [Windows Sync]","GetPrerequisiteKnowledge method [Windows Sync]","ISyncChangeWithPrerequisite interface","ISyncChangeWithPrerequisite interface [Windows Sync]","GetPrerequisiteKnowledge method","ISyncChangeWithPrerequisite.GetPrerequisiteKnowledge","ISyncChangeWithPrerequisite::GetPrerequisiteKnowledge","winsync.isyncchangewithprerequisite_getprerequisiteknowledge","winsync/ISyncChangeWithPrerequisite::GetPrerequisiteKnowledge"]
old-location: winsync\isyncchangewithprerequisite_getprerequisiteknowledge.htm
tech.root: winsync
ms.assetid: 48aa9436-b708-4dad-9201-d57988baf749
ms.date: 12/05/2018
ms.keywords: GetPrerequisiteKnowledge, GetPrerequisiteKnowledge method [Windows Sync], GetPrerequisiteKnowledge method [Windows Sync],ISyncChangeWithPrerequisite interface, ISyncChangeWithPrerequisite interface [Windows Sync],GetPrerequisiteKnowledge method, ISyncChangeWithPrerequisite.GetPrerequisiteKnowledge, ISyncChangeWithPrerequisite::GetPrerequisiteKnowledge, winsync.isyncchangewithprerequisite_getprerequisiteknowledge, winsync/ISyncChangeWithPrerequisite::GetPrerequisiteKnowledge
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
 - ISyncChangeWithPrerequisite::GetPrerequisiteKnowledge
 - winsync/ISyncChangeWithPrerequisite::GetPrerequisiteKnowledge
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
 - ISyncChangeWithPrerequisite.GetPrerequisiteKnowledge
---

# ISyncChangeWithPrerequisite::GetPrerequisiteKnowledge


## -description

Gets the minimum knowledge that a destination provider is required to have to process this change.

## -parameters

### -param ppPrerequisiteKnowledge [out]

The minimum knowledge that a destination provider is required to have to process this change.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
This object contains no prerequisite knowledge.

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

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangewithprerequisite">ISyncChangeWithPrerequisite Interface</a>