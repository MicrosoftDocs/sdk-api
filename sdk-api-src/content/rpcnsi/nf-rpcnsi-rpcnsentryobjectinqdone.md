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

# RpcNsEntryObjectInqDone function


## -description


The 
<b>RpcNsEntryObjectInqDone</b> function deletes the inquiry context for a name-service database entry's objects.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param InquiryContext

Pointer to a name-service handle specifying the object UUIDs exported to the <i>EntryName</i> parameter specified in the 
<a href="https://msdn.microsoft.com/dc667dc3-0812-43d5-adc2-aa29ee67f045">RpcNsEntryObjectInqBegin</a> function. 




An argument value of <b>NULL</b> is returned.


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
<b>RpcNsEntryObjectInqDone</b> function frees an inquiry context created by calling the 
<a href="https://msdn.microsoft.com/dc667dc3-0812-43d5-adc2-aa29ee67f045">RpcNsEntryObjectInqBegin</a> function.

An application calls 
<b>RpcNsEntryObjectInqDone</b> after viewing exported object UUIDs using the 
<a href="https://msdn.microsoft.com/95648480-5b53-4a8c-ba82-6c7f204520d2">RpcNsEntryObjectInqNext</a> function.




## -see-also




<a href="https://msdn.microsoft.com/dc667dc3-0812-43d5-adc2-aa29ee67f045">RpcNsEntryObjectInqBegin</a>



<a href="https://msdn.microsoft.com/95648480-5b53-4a8c-ba82-6c7f204520d2">RpcNsEntryObjectInqNext</a>
 

 

