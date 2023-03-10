---
UID: NF:winsync.ISyncKnowledge.ContainsChangeUnit
title: ISyncKnowledge::ContainsChangeUnit (winsync.h)
description: Indicates whether the specified change unit change is known by this knowledge.
helpviewer_keywords: ["ContainsChangeUnit","ContainsChangeUnit method [Windows Sync]","ContainsChangeUnit method [Windows Sync]","ISyncKnowledge interface","ISyncKnowledge interface [Windows Sync]","ContainsChangeUnit method","ISyncKnowledge.ContainsChangeUnit","ISyncKnowledge::ContainsChangeUnit","winsync.isyncknowledge_containschangeunit","winsync/ISyncKnowledge::ContainsChangeUnit"]
old-location: winsync\isyncknowledge_containschangeunit.htm
tech.root: winsync
ms.assetid: 67fc3b59-ad82-47a4-9fc6-2d980b9e26fe
ms.date: 12/05/2018
ms.keywords: ContainsChangeUnit, ContainsChangeUnit method [Windows Sync], ContainsChangeUnit method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],ContainsChangeUnit method, ISyncKnowledge.ContainsChangeUnit, ISyncKnowledge::ContainsChangeUnit, winsync.isyncknowledge_containschangeunit, winsync/ISyncKnowledge::ContainsChangeUnit
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
 - ISyncKnowledge::ContainsChangeUnit
 - winsync/ISyncKnowledge::ContainsChangeUnit
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
 - ISyncKnowledge.ContainsChangeUnit
---

# ISyncKnowledge::ContainsChangeUnit


## -description

Indicates whether the specified change unit change is known by this knowledge.

## -parameters

### -param pbVersionOwnerReplicaId [in]

The ID of the replica that originated the change unit change.

### -param pbItemId [in]

The ID of the item that contains the change unit to look up.

### -param pbChangeUnitId [in]

 The ID of the change unit to look up.

### -param pSyncVersion [in]

The version of the change unit change to look up.

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
The specified change unit change is contained in the knowledge.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified change unit change is not contained in the knowledge.

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