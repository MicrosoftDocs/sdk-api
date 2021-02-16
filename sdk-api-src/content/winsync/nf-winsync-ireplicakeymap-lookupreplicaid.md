---
UID: NF:winsync.IReplicaKeyMap.LookupReplicaId
title: IReplicaKeyMap::LookupReplicaId (winsync.h)
description: Gets the replica ID that corresponds to the specified replica key.
helpviewer_keywords: ["IReplicaKeyMap interface [Windows Sync]","LookupReplicaId method","IReplicaKeyMap.LookupReplicaId","IReplicaKeyMap::LookupReplicaId","LookupReplicaId","LookupReplicaId method [Windows Sync]","LookupReplicaId method [Windows Sync]","IReplicaKeyMap interface","winsync.ireplicakeymap_lookupreplicaid","winsync/IReplicaKeyMap::LookupReplicaId"]
old-location: winsync\ireplicakeymap_lookupreplicaid.htm
tech.root: winsync
ms.assetid: d76b5dbc-9ca1-4ba4-bdc2-99d31f1c9c8e
ms.date: 12/05/2018
ms.keywords: IReplicaKeyMap interface [Windows Sync],LookupReplicaId method, IReplicaKeyMap.LookupReplicaId, IReplicaKeyMap::LookupReplicaId, LookupReplicaId, LookupReplicaId method [Windows Sync], LookupReplicaId method [Windows Sync],IReplicaKeyMap interface, winsync.ireplicakeymap_lookupreplicaid, winsync/IReplicaKeyMap::LookupReplicaId
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
 - IReplicaKeyMap::LookupReplicaId
 - winsync/IReplicaKeyMap::LookupReplicaId
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
 - IReplicaKeyMap.LookupReplicaId
---

# IReplicaKeyMap::LookupReplicaId


## -description

Gets the replica ID that corresponds to the specified replica key.

## -parameters

### -param dwReplicaKey [in]

The replica key to look up.

### -param pbReplicaId [in, out]

Returns the replica ID that corresponds to <i>dwReplicaKey</i>.

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
<dt><b>SYNC_E_REPLICA_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
<i>dwReplicaKey</i> is not found.

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

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ireplicakeymap">IReplicaKeyMap Interface</a>