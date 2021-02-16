---
UID: NF:winsync.ISyncKnowledge.Serialize
title: ISyncKnowledge::Serialize (winsync.h)
description: Serializes the knowledge object data to a byte array.
helpviewer_keywords: ["ISyncKnowledge interface [Windows Sync]","Serialize method","ISyncKnowledge.Serialize","ISyncKnowledge::Serialize","Serialize","Serialize method [Windows Sync]","Serialize method [Windows Sync]","ISyncKnowledge interface","winsync.isyncknowledge_serialize","winsync/ISyncKnowledge::Serialize"]
old-location: winsync\isyncknowledge_serialize.htm
tech.root: winsync
ms.assetid: 1feb0626-78f0-4d37-b3a0-c87a7fb22753
ms.date: 12/05/2018
ms.keywords: ISyncKnowledge interface [Windows Sync],Serialize method, ISyncKnowledge.Serialize, ISyncKnowledge::Serialize, Serialize, Serialize method [Windows Sync], Serialize method [Windows Sync],ISyncKnowledge interface, winsync.isyncknowledge_serialize, winsync/ISyncKnowledge::Serialize
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
 - ISyncKnowledge::Serialize
 - winsync/ISyncKnowledge::Serialize
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
 - ISyncKnowledge.Serialize
---

# ISyncKnowledge::Serialize


## -description

Serializes the knowledge object data to a byte array.

## -parameters

### -param fSerializeReplicaKeyMap [in]

<b>TRUE</b> to serialize the <b>IReplicaKeyMap</b> object that is contained in the knowledge; otherwise, <b>FALSE</b>.

### -param pbKnowledge [in, out]

The byte array that receives the serialized knowledge data.

### -param pcbKnowledge [in, out]

Specifies the number of bytes in <i>pbKnowledge</i>. Returns the number of bytes required to serialize the replica key map data when <i>pbKnowledge</i> is too small, or returns the number of bytes written.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%"></td>
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
<i>pbKnowledge</i> is too small. In this case, the required number of bytes is returned in <i>pbKnowledge</i>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ireplicakeymap">IReplicaKeyMap Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>