---
UID: NF:winsync.ISyncChangeBatchBase2.SerializeWithOptions
title: ISyncChangeBatchBase2::SerializeWithOptions (winsync.h)
description: Serializes the change batch object data to a byte array, based on the specified version and serialization options.
helpviewer_keywords: ["ISyncChangeBatchBase2 interface [Windows Sync]","SerializeWithOptions method","ISyncChangeBatchBase2.SerializeWithOptions","ISyncChangeBatchBase2::SerializeWithOptions","SerializeWithOptions","SerializeWithOptions method [Windows Sync]","SerializeWithOptions method [Windows Sync]","ISyncChangeBatchBase2 interface","winsync.isyncchangebatchbase2_serializewithoptions","winsync/ISyncChangeBatchBase2::SerializeWithOptions"]
old-location: winsync\isyncchangebatchbase2_serializewithoptions.htm
tech.root: winsync
ms.assetid: 6e686e6f-08b1-4a58-ac0f-30c48f70dd60
ms.date: 12/05/2018
ms.keywords: ISyncChangeBatchBase2 interface [Windows Sync],SerializeWithOptions method, ISyncChangeBatchBase2.SerializeWithOptions, ISyncChangeBatchBase2::SerializeWithOptions, SerializeWithOptions, SerializeWithOptions method [Windows Sync], SerializeWithOptions method [Windows Sync],ISyncChangeBatchBase2 interface, winsync.isyncchangebatchbase2_serializewithoptions, winsync/ISyncChangeBatchBase2::SerializeWithOptions
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
 - ISyncChangeBatchBase2::SerializeWithOptions
 - winsync/ISyncChangeBatchBase2::SerializeWithOptions
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
 - ISyncChangeBatchBase2.SerializeWithOptions
---

# ISyncChangeBatchBase2::SerializeWithOptions


## -description

Serializes the change batch object data to a byte array, based on the specified version and serialization options.

## -parameters

### -param targetFormatVersion [in]

The serialized change batch is compatible with this version.

### -param dwFlags [in]

Reserved. Must be zero.

### -param pbBuffer [in, out]

The serialized change batch object data is serialized to this buffer.

### -param pdwSerializedSize [in, out]

The number of bytes in <i>pbBuffer</i>. Returns either the number of bytes that are required to serialize the change batch data when <i>pbBuffer</i> is too small, or the number of bytes written.

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
<i>dwFlags</i> is not zero, or the version that is specified by <i>targetFormatVersion</i> is incompatible with the change batch object data.

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
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The change batch contains a group that was started but not ended.

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

The following table describes the flags that specify information about an <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfilterinfo">ISyncFilterInfo</a> object.

<table>
<tr>
<th>SYNC_FILTER_INFO_FLAG value</th>
<th>Description </th>
</tr>
<tr>
<td><b>SYNC_FILTER_INFO_FLAG_ITEM_LIST</b></td>
<td>This flag indicates that the set of items synchronized is restricted by an item filter.


</td>
</tr>
<tr>
<td><b>SYNC_FILTER_INFO_FLAG_CHANGE_UNIT_LIST</b></td>
<td>An <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeunitlistfilterinfo">IChangeUnitListFilterInfo</a> object specifies that changes apply only to a subset of the change units that are defined for the scope.
</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase2">ISyncChangeBatchBase2 Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfilterinfo">ISyncFilterInfo Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge2">ISyncKnowledge2 Interface</a>



<a href="/windows/win32/api/winsync/ne-winsync-sync_serialization_version">SyncSerializationVersion Enumeration</a>