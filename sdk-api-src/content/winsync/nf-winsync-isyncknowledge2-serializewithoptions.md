---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ISyncKnowledge2::SerializeWithOptions


## -description


Serializes the knowledge object data to a byte array based on the specified version and serialization options.


## -parameters




### -param targetFormatVersion [in]

The serialized knowledge is compatible with this version.


### -param dwFlags [in]

Options that specify additional information about how to serialize the object. Must be zero or a combination of the values specified by the <b>SYNC_SERIALIZE</b> flags (see Remarks). When zero is specified, the replica key map is not included as part of the serialized knowledge data.


### -param pbBuffer




### -param pdwSerializedSize [in, out]

Specifies the number of bytes in <i>pBuffer</i>. Returns either the number of bytes that are required to serialize the knowledge data when <i>pBuffer</i> is too small, or the number of bytes written.


#### - pBuffer [in, out]

The serialized knowledge object data is serialized to this buffer.


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
<i>pBuffer</i> is too small. In this situation, the required number of bytes is returned in <i>pdwSerializedSize</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_VERSION</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>targetFormatVersion</i> is higher than the version of the object, or the object contains elements that are not compatible with <i>targetFormatVersion</i>.

</td>
</tr>
</table>
 




## -remarks



<b>Note</b>  The <b>SYNC_SERIALIZE</b> flags are defined as follows:<code>#define SYNC_SERIALIZE_REPLICA_KEY_MAP                 0x00000001</code>

The value <b>SYNC_SERIALIZE_REPLICA_KEY_MAP</b> indicates that the replica key map is included in the serialized knowledge data.



 When <b>SYNC_SERIALIZE_REPLICA_KEY_MAP</b> is specified for flags, the <b>IReplicaKeyMap</b> object is serialized along with the knowledge data. When this flag is not specified, the <b>IReplicaKeyMap</b> data must be stored in some other way so that the knowledge object can be deserialized.

The value of <i>targetFormatVersion</i> determines the format of the serialized knowledge data and refers to the version of <a href="http://go.microsoft.com/fwlink/p/?linkid=134798">Microsoft Sync Framework</a>. For an overview of what is involved in building synchronization providers using  <a href="http://go.microsoft.com/fwlink/p/?linkid=134798">Microsoft Sync Framework</a>, see <a href="https://msdn.microsoft.com/acf9a557-da4f-4688-9fea-9456947c17b4">Options for Building a Synchronization Provider</a>.




## -see-also




<a href="https://msdn.microsoft.com/3c195842-316a-4c49-ace4-444fa4a38ad2">IReplicaKeyMap Interface</a>



<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/1acbae32-8fa6-4c1e-95f6-30aca483c966">ISyncKnowledge2 Interface</a>



<a href="https://msdn.microsoft.com/acf9a557-da4f-4688-9fea-9456947c17b4">Options for Building a Synchronization Provider</a>
 

 

