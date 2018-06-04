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




<a href="https://msdn.microsoft.com/89a6d1c4-691d-4356-9ef5-1364b5a7507d">ISyncFilterInfo Interface</a>
 

 

