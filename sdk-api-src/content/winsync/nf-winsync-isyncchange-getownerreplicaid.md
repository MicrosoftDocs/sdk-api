---
UID: NF:winsync.ISyncChange.GetOwnerReplicaId
title: ISyncChange::GetOwnerReplicaId (winsync.h)
description: Gets the ID of the replica that originated this change.
helpviewer_keywords: ["GetOwnerReplicaId","GetOwnerReplicaId method [Windows Sync]","GetOwnerReplicaId method [Windows Sync]","ISyncChange interface","ISyncChange interface [Windows Sync]","GetOwnerReplicaId method","ISyncChange.GetOwnerReplicaId","ISyncChange::GetOwnerReplicaId","winsync.isyncchange_getownerreplicaid","winsync/ISyncChange::GetOwnerReplicaId"]
old-location: winsync\isyncchange_getownerreplicaid.htm
tech.root: winsync
ms.assetid: c65dc19e-e11a-4bd1-b10f-f2af75294d48
ms.date: 12/05/2018
ms.keywords: GetOwnerReplicaId, GetOwnerReplicaId method [Windows Sync], GetOwnerReplicaId method [Windows Sync],ISyncChange interface, ISyncChange interface [Windows Sync],GetOwnerReplicaId method, ISyncChange.GetOwnerReplicaId, ISyncChange::GetOwnerReplicaId, winsync.isyncchange_getownerreplicaid, winsync/ISyncChange::GetOwnerReplicaId
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
 - ISyncChange::GetOwnerReplicaId
 - winsync/ISyncChange::GetOwnerReplicaId
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
 - ISyncChange.GetOwnerReplicaId
---

# ISyncChange::GetOwnerReplicaId


## -description

Gets the ID of the replica that originated this change.

## -parameters

### -param pbReplicaId [in, out]

Returns the ID of the replica that originated this change.

### -param pcbIdSize [in, out]

Specifies the number of bytes in <i>pbReplicaId</i>. Returns the number of bytes required to retrieve the ID when <i>pbReplicaId</i> is too small, or returns the number of bytes written.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pbReplicaId</i> is too small. In this case, the required number of bytes is returned in <i>pcbIdSize</i>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchange">ISyncChange Interface</a>