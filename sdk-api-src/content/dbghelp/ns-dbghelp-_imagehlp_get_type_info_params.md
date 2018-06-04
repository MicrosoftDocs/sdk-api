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

# _IMAGEHLP_GET_TYPE_INFO_PARAMS structure


## -description


Contains type information for a module.


## -struct-fields




### -field SizeOfStruct

The size of this structure, in bytes.


### -field Flags

This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMAGEHLP_GET_TYPE_INFO_CHILDREN"></a><a id="imagehlp_get_type_info_children"></a><dl>
<dt><b>IMAGEHLP_GET_TYPE_INFO_CHILDREN</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Retrieve information about the children of the specified types, not the types themselves.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGEHLP_GET_TYPE_INFO_UNCACHED"></a><a id="imagehlp_get_type_info_uncached"></a><dl>
<dt><b>IMAGEHLP_GET_TYPE_INFO_UNCACHED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Do not cache the data for later retrievals. It is good to use this flag if you will not be requesting the information again.

</td>
</tr>
</table>
 


### -field NumIds

The number of elements specified in the <b>TypeIds</b> array.


### -field TypeIds

An array of type indexes.


### -field TagFilter

The filter for return values. For example, set this member to 1 &lt;&lt; <b>SymTagData</b> to return only results with a symbol tag of <b>SymTagData</b>. For a list of tags, see the <b>SymTagEnum</b> type defined in Dbghelp.h


### -field NumReqs

The number of elements specified in the arrays specified in the <b>ReqKinds</b>, <b>ReqOffsets</b>, and <b>ReqSizes</b> members. These arrays must be the same size.


### -field ReqKinds

An array of information types to be requested. Each element is one of the enumeration values in the <a href="https://msdn.microsoft.com/1b21c8dc-240f-4202-bd61-8f9dae0d053a">IMAGEHLP_SYMBOL_TYPE_INFO</a> enumeration type.


### -field ReqOffsets

An array of offsets that specify where to store the data for each request within each element of <b>Buffer</b> array.


### -field ReqSizes

The size of each data request, in bytes. The required sizes are described in <a href="https://msdn.microsoft.com/1b21c8dc-240f-4202-bd61-8f9dae0d053a">IMAGEHLP_SYMBOL_TYPE_INFO</a>.


### -field ReqStride

The number of bytes for each element in the <b>Buffer</b> array.


### -field BufferSize

The size of the <b>Buffer</b> array, in bytes.


### -field Buffer

An array of records used for storing query results. Each record is separated by <b>ReqStride</b> bytes. Each type for which data is to be retrieved requires one record in the array. Within each record, there are <b>NumReqs</b> pieces of data stored as the result of individual queries. The data is stored within the record according to the offsets specified in <b>ReqOffsets</b>. The format of the data depends on the value of the <b>ReqKinds</b> member in use.


### -field EntriesMatched

The number of type entries that match the filter.


### -field EntriesFilled

The number of elements in the <b>Buffer</b> array that received results.


### -field TagsFound

A bitmask indicating all tag bits encountered during the search operation.


### -field AllReqsValid

A bitmask indicate the bit-wise AND of all <b>ReqsValid</b> fields.


### -field NumReqsValid

The size of <b>ReqsValid</b>, in elements.


### -field OPTIONAL

 




#### - ReqsValid

A bitmask indexed by <b>Buffer</b> element index that indicates which request data is valid. This member can be <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/1b21c8dc-240f-4202-bd61-8f9dae0d053a">IMAGEHLP_SYMBOL_TYPE_INFO</a>



<a href="https://msdn.microsoft.com/77e0a8ad-8c75-4bb2-869a-670429475ccc">SymGetTypeInfoEx</a>
 

 

