---
UID: NF:winsync.ISyncChangeBatchBase2.SerializeWithOptions
title: ISyncChangeBatchBase2::SerializeWithOptions
author: windows-sdk-content
description: Serializes the change batch object data to a byte array, based on the specified version and serialization options.
old-location: winsync\isyncchangebatchbase2_serializewithoptions.htm
old-project: winsync
ms.assetid: 6e686e6f-08b1-4a58-ac0f-30c48f70dd60
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ISyncChangeBatchBase2 interface [Windows Sync],SerializeWithOptions method, ISyncChangeBatchBase2.SerializeWithOptions, ISyncChangeBatchBase2::SerializeWithOptions, SerializeWithOptions, SerializeWithOptions method [Windows Sync], SerializeWithOptions method [Windows Sync],ISyncChangeBatchBase2 interface, winsync.isyncchangebatchbase2_serializewithoptions, winsync/ISyncChangeBatchBase2::SerializeWithOptions
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
 - ISyncChangeBatchBase2.SerializeWithOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



The following table describes the flags that specify information about an <a href="https://msdn.microsoft.com/89a6d1c4-691d-4356-9ef5-1364b5a7507d">ISyncFilterInfo</a> object.

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
<td>An <a href="https://msdn.microsoft.com/fd379fc6-22e5-4165-b4e6-480bc65cccb3">IChangeUnitListFilterInfo</a> object specifies that changes apply only to a subset of the change units that are defined for the scope.
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase Interface</a>



<a href="https://msdn.microsoft.com/45f10ed0-b3ce-41f5-b2d9-9166bff2abec">ISyncChangeBatchBase2 Interface</a>



<a href="https://msdn.microsoft.com/89a6d1c4-691d-4356-9ef5-1364b5a7507d">ISyncFilterInfo Interface</a>



<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/1acbae32-8fa6-4c1e-95f6-30aca483c966">ISyncKnowledge2 Interface</a>



<a href="https://msdn.microsoft.com/840a1f5e-56f7-4774-a154-0dab66c3d407">SyncSerializationVersion Enumeration</a>
 

 

