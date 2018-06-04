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

# RpcIfIdVectorFree function


## -description


The 
<b>RpcIfIdVectorFree</b> function frees the vector and the interface-identification structures contained in the vector.


## -parameters




### -param IfIdVector

TBD




#### - IfIdVec

Address of a pointer to a vector of interface information. On return, the pointer is set to <b>NULL</b>.


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
<dt><b>RPC_S_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
The argument was invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



An application calls the 
<b>RpcIfIdVectorFree</b> function to release the memory used to store a vector of interface identifications. 
<b>RpcIfIdVectorFree</b> frees memory containing the interface identifications and the vector itself. On return, this function sets the <i>IfIdVec</i> parameter to <b>NULL</b>.

An application obtains a vector of interface identifications by calling the 
<a href="https://msdn.microsoft.com/92f33e1d-a054-4484-903a-c91d3cd549d1">RpcNsMgmtEntryInqIfIds</a> and 
<a href="https://msdn.microsoft.com/f6d89f2c-ff51-44ab-9f8a-2f76cd3ac6db">RpcMgmtInqIfIds</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/1b91e88c-b242-472f-b719-60f96599cb67">RpcIfInqId</a>



<a href="https://msdn.microsoft.com/f6d89f2c-ff51-44ab-9f8a-2f76cd3ac6db">RpcMgmtInqIfIds</a>



<a href="https://msdn.microsoft.com/92f33e1d-a054-4484-903a-c91d3cd549d1">RpcNsMgmtEntryInqIfIds</a>
 

 

