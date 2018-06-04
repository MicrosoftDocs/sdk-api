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

# RpcMgmtEpEltInqDone function


## -description


The 
<b>RpcMgmtEpEltInqDone</b> function deletes the inquiry context for viewing the elements in an endpoint map.


## -parameters




### -param InquiryContext

Inquiry context to delete and returns the value <b>NULL</b>.


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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcMgmtEpEltInqDone</b> function deletes an inquiry context created by 
<a href="https://msdn.microsoft.com/659ab657-e17f-46a9-942e-aa2631c1716d">RpcMgmtEpEltInqBegin</a>. An application calls this function after viewing local endpoint-map elements using 
<a href="https://msdn.microsoft.com/e1f79435-6868-453b-8237-da52e57ec96f">RpcMgmtEpEltInqNext</a>.




## -see-also




<a href="https://msdn.microsoft.com/35656cdd-b1ae-43d3-a5c7-92bdb7726d5b">RpcEpRegister</a>



<a href="https://msdn.microsoft.com/659ab657-e17f-46a9-942e-aa2631c1716d">RpcMgmtEpEltInqBegin</a>



<a href="https://msdn.microsoft.com/e1f79435-6868-453b-8237-da52e57ec96f">RpcMgmtEpEltInqNext</a>
 

 

