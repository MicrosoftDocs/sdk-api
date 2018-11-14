---
UID: NF:winsync.IReplicaKeyMap.LookupReplicaKey
title: IReplicaKeyMap::LookupReplicaKey
author: windows-sdk-content
description: Gets the replica key that corresponds to the specified replica ID.
old-location: winsync\ireplicakeymap_lookupreplicakey.htm
tech.root: winsync
ms.assetid: 92bae64f-67a5-4029-9d24-eee92a3fc55f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IReplicaKeyMap interface [Windows Sync],LookupReplicaKey method, IReplicaKeyMap.LookupReplicaKey, IReplicaKeyMap::LookupReplicaKey, LookupReplicaKey, LookupReplicaKey method [Windows Sync], LookupReplicaKey method [Windows Sync],IReplicaKeyMap interface, winsync.ireplicakeymap_lookupreplicakey, winsync/IReplicaKeyMap::LookupReplicaKey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IReplicaKeyMap.LookupReplicaKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- winsync.h
: 
- IReplicaKeyMap.LookupReplicaKey
: 
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




<a href="https://msdn.microsoft.com/3c195842-316a-4c49-ace4-444fa4a38ad2">IReplicaKeyMap Interface</a>
 

 

