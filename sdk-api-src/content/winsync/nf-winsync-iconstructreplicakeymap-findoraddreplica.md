---
UID: NF:winsync.IConstructReplicaKeyMap.FindOrAddReplica
title: IConstructReplicaKeyMap::FindOrAddReplica
author: windows-sdk-content
description: Adds entries to or finds entries in an IReplicaKeyMap object.
old-location: winsync\iconstructreplicakeymap_findoraddreplica.htm
old-project: winsync
ms.assetid: 10cf616c-a082-4a74-99bb-1b0b364291e5
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: FindOrAddReplica, FindOrAddReplica method [Windows Sync], FindOrAddReplica method [Windows Sync],IConstructReplicaKeyMap interface, IConstructReplicaKeyMap interface [Windows Sync],FindOrAddReplica method, IConstructReplicaKeyMap.FindOrAddReplica, IConstructReplicaKeyMap::FindOrAddReplica, winsync.iconstructreplicakeymap_findoraddreplica, winsync/IConstructReplicaKeyMap::FindOrAddReplica
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IConstructReplicaKeyMap.FindOrAddReplica
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IConstructReplicaKeyMap::FindOrAddReplica


## -description


Adds entries to or finds entries in an <b>IReplicaKeyMap</b> object.


## -parameters




### -param pbReplicaId [in]

The ID of the replica to add or find.


### -param pdwReplicaKey [out]

The key of the replica in the map. If an entry for <i>pbReplicaId</i> does not exist in the map, an entry is created and a new key is assigned to it.


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
<dt><b>SYNC_E_ID_FORMAT_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
<i>pbReplicaId</i> is not of the format that the provider specified.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/742b5606-5d24-4494-9f96-e381af1145db">IConstructReplicaKeyMap Interface</a>
 

 

