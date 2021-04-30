---
UID: NF:winsync.ISyncKnowledge2.SerializeWithOptions
title: ISyncKnowledge2::SerializeWithOptions (winsync.h)
description: Serializes the knowledge object data to a byte array based on the specified version and serialization options.
helpviewer_keywords: ["ISyncKnowledge2 interface [Windows Sync]","SerializeWithOptions method","ISyncKnowledge2.SerializeWithOptions","ISyncKnowledge2::SerializeWithOptions","SerializeWithOptions","SerializeWithOptions method [Windows Sync]","SerializeWithOptions method [Windows Sync]","ISyncKnowledge2 interface","winsync.isyncknowledge2_serializewithoptions","winsync/ISyncKnowledge2::SerializeWithOptions"]
old-location: winsync\isyncknowledge2_serializewithoptions.htm
tech.root: winsync
ms.assetid: b8b9084f-f4aa-42b8-8c45-ed075db8ffe4
ms.date: 12/05/2018
ms.keywords: ISyncKnowledge2 interface [Windows Sync],SerializeWithOptions method, ISyncKnowledge2.SerializeWithOptions, ISyncKnowledge2::SerializeWithOptions, SerializeWithOptions, SerializeWithOptions method [Windows Sync], SerializeWithOptions method [Windows Sync],ISyncKnowledge2 interface, winsync.isyncknowledge2_serializewithoptions, winsync/ISyncKnowledge2::SerializeWithOptions
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
 - ISyncKnowledge2::SerializeWithOptions
 - winsync/ISyncKnowledge2::SerializeWithOptions
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
 - ISyncKnowledge2.SerializeWithOptions
---

# ISyncKnowledge2::SerializeWithOptions


## -description

Serializes the knowledge object data to a byte array based on the specified version and serialization options.

## -parameters

### -param targetFormatVersion [in]

The serialized knowledge is compatible with this version.

### -param dwFlags [in]

Options that specify additional information about how to serialize the object. Must be zero or a combination of the values specified by the <b>SYNC_SERIALIZE</b> flags (see Remarks). When zero is specified, the replica key map is not included as part of the serialized knowledge data.

### -param pbBuffer [in, out]

The serialized knowledge object data is serialized to this buffer.

### -param pdwSerializedSize [in, out]

Specifies the number of bytes in <i>pBuffer</i>. Returns either the number of bytes that are required to serialize the knowledge data when <i>pBuffer</i> is too small, or the number of bytes written.

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

The value of <i>targetFormatVersion</i> determines the format of the serialized knowledge data and refers to the version of <a href="https://www.microsoft.com/downloads/details.aspx?familyid=A3EE7BC5-A823-4FB4-B152-9E8CE9D5546F&displaylang=en">Microsoft Sync Framework</a>. For an overview of what is involved in building synchronization providers using  <a href="https://www.microsoft.com/downloads/details.aspx?familyid=A3EE7BC5-A823-4FB4-B152-9E8CE9D5546F&displaylang=en">Microsoft Sync Framework</a>, see <a href="/previous-versions/windows/desktop/winsync/options-for-building-a-synchronization-provider">Options for Building a Synchronization Provider</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ireplicakeymap">IReplicaKeyMap Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge2">ISyncKnowledge2 Interface</a>



<a href="/previous-versions/windows/desktop/winsync/options-for-building-a-synchronization-provider">Options for Building a Synchronization Provider</a>