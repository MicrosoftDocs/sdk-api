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

# RpcNsProfileEltInqDone function


## -description


The 
<b>RpcNsProfileEltInqDone</b> function deletes the inquiry context for viewing the elements in a profile.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param InquiryContext

Pointer to a name-service handle to free. The name-service handle that <i>InquiryContext</i> points to is created by calling the 
<a href="https://msdn.microsoft.com/5b14eb21-0c3e-4f12-b1dc-95b364d87a4f">RpcNsProfileEltInqBegin</a> function. 




An argument value of NULL is returned.


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
<b>RpcNsProfileEltInqDone</b> function frees an inquiry context created by calling 
<a href="https://msdn.microsoft.com/5b14eb21-0c3e-4f12-b1dc-95b364d87a4f">RpcNsProfileEltInqBegin</a>.

An application calls 
<b>RpcNsProfileEltInqDone</b> after viewing profile elements using the 
<a href="https://msdn.microsoft.com/78835fde-82c3-4cff-94b9-91e07120e03f">RpcNsProfileEltInqNext</a> function.

<div class="alert"><b>Note</b>  Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/5b14eb21-0c3e-4f12-b1dc-95b364d87a4f">RpcNsProfileEltInqBegin</a>



<a href="https://msdn.microsoft.com/78835fde-82c3-4cff-94b9-91e07120e03f">RpcNsProfileEltInqNext</a>
 

 

