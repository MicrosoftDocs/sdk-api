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

# RpcNsGroupMbrInqDone function


## -description


The 
<b>RpcNsGroupMbrInqDone</b> function deletes the inquiry context for a group.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param InquiryContext

Pointer to a name-service handle to free. A value of NULL is returned.


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
<dt><b>RPC_S_INVALID_NS_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The name-service handle is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcNsGroupMbrInqDone</b> function frees an inquiry context created by calling the 
<a href="https://msdn.microsoft.com/f3a98563-0c7f-4f4b-b272-af7c0366b95d">RpcNsGroupMbrInqBegin</a> function. An application calls 
<b>RpcNsGroupMbrInqDone</b> after viewing RPC group members using the 
<a href="https://msdn.microsoft.com/58f32594-85de-4d20-86b2-210367ccb7ce">RpcNsGroupMbrInqNext</a> function.

<div class="alert"><b>Note</b>  Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f3a98563-0c7f-4f4b-b272-af7c0366b95d">RpcNsGroupMbrInqBegin</a>



<a href="https://msdn.microsoft.com/58f32594-85de-4d20-86b2-210367ccb7ce">RpcNsGroupMbrInqNext</a>
 

 

