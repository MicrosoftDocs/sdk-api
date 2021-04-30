---
UID: NF:winsync.ISyncFilterInfo.Serialize
title: ISyncFilterInfo::Serialize (winsync.h)
description: Serializes the filter data to an array of bytes.
helpviewer_keywords: ["ISyncFilterInfo interface [Windows Sync]","Serialize method","ISyncFilterInfo.Serialize","ISyncFilterInfo::Serialize","Serialize","Serialize method [Windows Sync]","Serialize method [Windows Sync]","ISyncFilterInfo interface","winsync.isyncfilterinfo_serialize","winsync/ISyncFilterInfo::Serialize"]
old-location: winsync\isyncfilterinfo_serialize.htm
tech.root: winsync
ms.assetid: bd3e9fec-9fa2-4216-9a05-1f121bd3dbef
ms.date: 12/05/2018
ms.keywords: ISyncFilterInfo interface [Windows Sync],Serialize method, ISyncFilterInfo.Serialize, ISyncFilterInfo::Serialize, Serialize, Serialize method [Windows Sync], Serialize method [Windows Sync],ISyncFilterInfo interface, winsync.isyncfilterinfo_serialize, winsync/ISyncFilterInfo::Serialize
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
 - ISyncFilterInfo::Serialize
 - winsync/ISyncFilterInfo::Serialize
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
 - ISyncFilterInfo.Serialize
---

# ISyncFilterInfo::Serialize


## -description

Serializes the filter data to an array of bytes.

## -parameters

### -param pbBuffer [in, out]

Returns the serialized filter information. Set this value to <b>NULL</b> to request the required size of the buffer.

### -param pcbBuffer [in, out]

Specifies the number of bytes in <i>pbBuffer</i>. Returns the number of bytes required to serialize the filter when <i>pcbBuffer</i> is too small, or the number of bytes written.

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
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0x800700EA (HRESULT_FROM_WIN32(ERROR_MORE_DATA))</b></dt>
</dl>
</td>
<td width="60%">
<i>pbBuffer</i> is <b>NULL</b> or <i>pcbBuffer</i> is too small. In this case, the number of bytes required to serialize the filter is returned in <i>pcbBuffer</i>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfilterinfo">ISyncFilterInfo Interface</a>