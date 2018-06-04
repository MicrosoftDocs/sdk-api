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

# MesHandleFree function


## -description


The 
<b>MesHandleFree</b> function frees the memory allocated by the serialization handle.


## -parameters




### -param Handle

Handle to be freed.


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
<b>MesHandleFree</b> routine is used by applications to free the resources of the handle after encoding or decoding data.




## -see-also




<a href="https://msdn.microsoft.com/10a2312d-5969-4dde-bf62-308ad425569b">MesDecodeBufferHandleCreate</a>



<a href="https://msdn.microsoft.com/4d8cb8e3-aa5a-4354-87e7-57543baa57e8">MesEncodeDynBufferHandleCreate</a>



<a href="https://msdn.microsoft.com/7700e0f6-0f30-415c-9873-983ec6c249b2">MesEncodeFixedBufferHandleCreate</a>



<a href="https://msdn.microsoft.com/54bbe560-08a9-4e41-9121-37aab0c209a9">MesEncodeIncrementalHandleCreate</a>
 

 

