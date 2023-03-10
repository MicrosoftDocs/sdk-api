---
UID: NF:winsync.ISyncChangeBatchBase.Serialize
title: ISyncChangeBatchBase::Serialize (winsync.h)
description: Serializes the change batch to an array of bytes.
helpviewer_keywords: ["ISyncChangeBatchBase interface [Windows Sync]","Serialize method","ISyncChangeBatchBase.Serialize","ISyncChangeBatchBase::Serialize","Serialize","Serialize method [Windows Sync]","Serialize method [Windows Sync]","ISyncChangeBatchBase interface","winsync.isyncchangebatchbase_serialize","winsync/ISyncChangeBatchBase::Serialize"]
old-location: winsync\isyncchangebatchbase_serialize.htm
tech.root: winsync
ms.assetid: 785a763c-99a2-45d1-b42b-9673aedc5c5d
ms.date: 12/05/2018
ms.keywords: ISyncChangeBatchBase interface [Windows Sync],Serialize method, ISyncChangeBatchBase.Serialize, ISyncChangeBatchBase::Serialize, Serialize, Serialize method [Windows Sync], Serialize method [Windows Sync],ISyncChangeBatchBase interface, winsync.isyncchangebatchbase_serialize, winsync/ISyncChangeBatchBase::Serialize
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
 - ISyncChangeBatchBase::Serialize
 - winsync/ISyncChangeBatchBase::Serialize
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
 - ISyncChangeBatchBase.Serialize
---

# ISyncChangeBatchBase::Serialize


## -description

Serializes the change batch to an array of bytes.

## -parameters

### -param pbChangeBatch [in, out]

The byte array that receives the change batch data.

### -param pcbChangeBatch [in, out]

Specifies the number of bytes in <i>pbChangeBatch</i>. Returns the number of bytes required for <i>pbChangeBatch</i> when <i>pbChangeBatch</i> is too small, or the number of bytes written to <i>pbChangeBatch</i> when data is written.

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
<i>pbChangeBatch</i> is too small. In this case, the required number of bytes is stored in <i>pcbChangeBatch</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The last group added to the batch was not ended.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>



<a href="/windows/win32/api/winsync/ne-winsync-sync_serialization_version">SyncSerializationVersion Enumeration</a>