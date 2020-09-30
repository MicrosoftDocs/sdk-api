---
UID: NF:winsync.ISyncChangeBatchBase.GetPrerequisiteKnowledge
title: ISyncChangeBatchBase::GetPrerequisiteKnowledge (winsync.h)
description: Gets the minimum knowledge that a destination provider is required to have to process this change batch.
helpviewer_keywords: ["GetPrerequisiteKnowledge","GetPrerequisiteKnowledge method [Windows Sync]","GetPrerequisiteKnowledge method [Windows Sync]","ISyncChangeBatchBase interface","ISyncChangeBatchBase interface [Windows Sync]","GetPrerequisiteKnowledge method","ISyncChangeBatchBase.GetPrerequisiteKnowledge","ISyncChangeBatchBase::GetPrerequisiteKnowledge","winsync.isyncchangebatchbase_getprerequisiteknowledge","winsync/ISyncChangeBatchBase::GetPrerequisiteKnowledge"]
old-location: winsync\isyncchangebatchbase_getprerequisiteknowledge.htm
tech.root: winsync
ms.assetid: dd078725-7fd8-4d6c-9b43-f6741b03f1e6
ms.date: 12/05/2018
ms.keywords: GetPrerequisiteKnowledge, GetPrerequisiteKnowledge method [Windows Sync], GetPrerequisiteKnowledge method [Windows Sync],ISyncChangeBatchBase interface, ISyncChangeBatchBase interface [Windows Sync],GetPrerequisiteKnowledge method, ISyncChangeBatchBase.GetPrerequisiteKnowledge, ISyncChangeBatchBase::GetPrerequisiteKnowledge, winsync.isyncchangebatchbase_getprerequisiteknowledge, winsync/ISyncChangeBatchBase::GetPrerequisiteKnowledge
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
 - ISyncChangeBatchBase::GetPrerequisiteKnowledge
 - winsync/ISyncChangeBatchBase::GetPrerequisiteKnowledge
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
 - ISyncChangeBatchBase.GetPrerequisiteKnowledge
---

# ISyncChangeBatchBase::GetPrerequisiteKnowledge


## -description

Gets the minimum knowledge that a destination provider is required to have to process this change batch.

## -parameters

### -param ppPrerequisteKnowledge [out]

Returns the minimum knowledge that a destination provider is required to have to process this change batch.

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

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>