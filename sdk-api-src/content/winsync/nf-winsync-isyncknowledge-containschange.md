---
UID: NF:winsync.ISyncKnowledge.ContainsChange
title: ISyncKnowledge::ContainsChange (winsync.h)
description: Indicates whether the specified item change is known by this knowledge.
helpviewer_keywords: ["ContainsChange","ContainsChange method [Windows Sync]","ContainsChange method [Windows Sync]","ISyncKnowledge interface","ISyncKnowledge interface [Windows Sync]","ContainsChange method","ISyncKnowledge.ContainsChange","ISyncKnowledge::ContainsChange","winsync.isyncknowledge_containschange","winsync/ISyncKnowledge::ContainsChange"]
old-location: winsync\isyncknowledge_containschange.htm
tech.root: winsync
ms.assetid: 4c304d76-f27a-4382-99ad-1d158da93de6
ms.date: 12/05/2018
ms.keywords: ContainsChange, ContainsChange method [Windows Sync], ContainsChange method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],ContainsChange method, ISyncKnowledge.ContainsChange, ISyncKnowledge::ContainsChange, winsync.isyncknowledge_containschange, winsync/ISyncKnowledge::ContainsChange
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
 - ISyncKnowledge::ContainsChange
 - winsync/ISyncKnowledge::ContainsChange
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
 - ISyncKnowledge.ContainsChange
---

# ISyncKnowledge::ContainsChange


## -description

Indicates whether the specified item change is known by this knowledge.

## -parameters

### -param pbVersionOwnerReplicaId [in]

The ID of the replica that originated the change.

### -param pgidItemId [in]

The ID of the item that changed.

### -param pSyncVersion [in]

The version of the change.

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
The specified change is not contained in the knowledge.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="/windows/desktop/api/winsync/ns-winsync-sync_version">SYNC_VERSION Structure</a>