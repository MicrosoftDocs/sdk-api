---
UID: NF:winsync.IReplicaKeyMap.LookupReplicaKey
title: IReplicaKeyMap::LookupReplicaKey (winsync.h)
description: Gets the replica key that corresponds to the specified replica ID.
helpviewer_keywords: ["IReplicaKeyMap interface [Windows Sync]","LookupReplicaKey method","IReplicaKeyMap.LookupReplicaKey","IReplicaKeyMap::LookupReplicaKey","LookupReplicaKey","LookupReplicaKey method [Windows Sync]","LookupReplicaKey method [Windows Sync]","IReplicaKeyMap interface","winsync.ireplicakeymap_lookupreplicakey","winsync/IReplicaKeyMap::LookupReplicaKey"]
old-location: winsync\ireplicakeymap_lookupreplicakey.htm
tech.root: winsync
ms.assetid: 92bae64f-67a5-4029-9d24-eee92a3fc55f
ms.date: 12/05/2018
ms.keywords: IReplicaKeyMap interface [Windows Sync],LookupReplicaKey method, IReplicaKeyMap.LookupReplicaKey, IReplicaKeyMap::LookupReplicaKey, LookupReplicaKey, LookupReplicaKey method [Windows Sync], LookupReplicaKey method [Windows Sync],IReplicaKeyMap interface, winsync.ireplicakeymap_lookupreplicakey, winsync/IReplicaKeyMap::LookupReplicaKey
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
 - IReplicaKeyMap::LookupReplicaKey
 - winsync/IReplicaKeyMap::LookupReplicaKey
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
 - IReplicaKeyMap.LookupReplicaKey
---

# IReplicaKeyMap::LookupReplicaKey


## -description

Gets the replica key that corresponds to the specified replica ID.

## -parameters

### -param pbReplicaId [in]

The replica ID to look up.

### -param pdwReplicaKey [out]

Returns the replica key that corresponds to <i>pbReplicaId</i>.

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
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_ID_FORMAT_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
When <i>pbReplicaId</i> is not in the format that is specified by the ID format schema of the provider.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_REPLICA_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
When <i>pbReplicaId</i> is not found.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ireplicakeymap">IReplicaKeyMap Interface</a>