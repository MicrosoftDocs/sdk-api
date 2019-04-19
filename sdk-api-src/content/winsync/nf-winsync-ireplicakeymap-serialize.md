---
UID: NF:winsync.IReplicaKeyMap.Serialize
title: IReplicaKeyMap::Serialize (winsync.h)
author: windows-sdk-content
description: Serializes the replica key map data to a byte array.
old-location: winsync\ireplicakeymap_serialize.htm
tech.root: winsync
ms.assetid: 0ed19406-82b8-428f-bed2-796e287dd4cb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IReplicaKeyMap interface [Windows Sync],Serialize method, IReplicaKeyMap.Serialize, IReplicaKeyMap::Serialize, Serialize, Serialize method [Windows Sync], Serialize method [Windows Sync],IReplicaKeyMap interface, winsync.ireplicakeymap_serialize, winsync/IReplicaKeyMap::Serialize
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
 - IReplicaKeyMap.Serialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IReplicaKeyMap::Serialize


## -description


Serializes the replica key map data to a byte array.


## -parameters




### -param pbReplicaKeyMap [in, out]

The byte array that receives the serialized data.


### -param pcbReplicaKeyMap [in, out]

Specifies the number of bytes in <i>pbReplicaKeyMap</i>. Returns the number of bytes required to serialize the replica key map data when <i>pbReplicaKeyMap</i> is too small, or returns the number of bytes written.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A replica ID or replica key stored in the map is not valid.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pbReplicaKeyMap</i> is too small. In this case, the required number of bytes is returned in <i>pcbReplicaKeyMap</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3c195842-316a-4c49-ace4-444fa4a38ad2">IReplicaKeyMap Interface</a>
 

 

