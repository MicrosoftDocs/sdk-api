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

# RpcObjectInqType function


## -description


The 
<b>RpcObjectInqType</b> function returns the type of an object.


## -parameters




### -param ObjUuid

Pointer to the object UUID whose associated type UUID is returned.


### -param TypeUuid

Returns a pointer to the type UUID of the <i>ObjUuid</i> parameter. 




Specify a parameter value of <b>NULL</b> to prevent the return of a type UUID. In this way, an application can determine (from the returned status) whether <i>ObjUuid</i> is registered without specifying an output type UUID variable.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Object not found.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



A server application calls 
<b>RpcObjectInqType</b> to obtain the type UUID of an object. If the object was registered with the RPC run-time library using the 
<a href="https://msdn.microsoft.com/2fb22b97-97ce-403a-bfcb-101bb63f906f">RpcObjectSetType</a> function, the registered type is returned.

Optionally, an application can privately maintain an object/type registration. In this case, if the application has provided an object inquiry function (see under 
<a href="https://msdn.microsoft.com/358d3ab3-df16-486b-aeac-56a0ffc78272">RpcObjectSetInqFn</a>). The RPC run-time library uses that function to determine an object's type.

The 
<b>RpcObjectInqType</b> function obtains the type UUID as described in the following table.

<table>
<tr>
<th>Object UUID<div> </div>
registered</th>
<th>Inquiry function<div> </div>
registered</th>
<th>Return<div> </div>
value</th>
</tr>
<tr>
<td>Yes (
<a href="https://msdn.microsoft.com/2fb22b97-97ce-403a-bfcb-101bb63f906f">RpcObjectSetType</a>)</td>
<td>Ignored</td>
<td>The object's registered type UUID.</td>
</tr>
<tr>
<td>No</td>
<td>Yes (
<a href="https://msdn.microsoft.com/358d3ab3-df16-486b-aeac-56a0ffc78272">RpcObjectSetInqFn</a>)</td>
<td>The type UUID returned from the inquiry function.</td>
</tr>
<tr>
<td>No</td>
<td>No</td>
<td>The nil UUID.</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/358d3ab3-df16-486b-aeac-56a0ffc78272">RpcObjectSetInqFn</a>



<a href="https://msdn.microsoft.com/2fb22b97-97ce-403a-bfcb-101bb63f906f">RpcObjectSetType</a>
 

 

