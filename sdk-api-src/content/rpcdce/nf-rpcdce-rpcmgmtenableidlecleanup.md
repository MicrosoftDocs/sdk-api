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

# RpcMgmtEnableIdleCleanup function


## -description


The 
<b>RpcMgmtEnableIdleCleanup</b> function enables RPC to close idle resources, such as network connections, on the client.


## -parameters






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
<dt><b>RPC_S_OUT_OF_THREADS</b></dt>
</dl>
</td>
<td width="60%">
Out of threads.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OUT_OF_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
Out of resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



<div class="alert"><b>Note</b>  <b>RpcMgmtEnableIdleCleanup</b> is a Microsoft extension to the OSF-DCE RPC specification.</div>
<div> </div>
Calling this function only is sufficient. Once called, idle resource cleanup cannot be turned off. In some cases, depending on Windows version and configuration, RPC Runtime may need to create a separate thread in order to perform such cleanup, which is why idle resource cleanup is not always turned on. On Windows XP and later versions of Windows, RPC Runtime is programmed to automatically turn on idle resource cleanup if idle resources reach a certain threshold.




## -see-also




<a href="https://msdn.microsoft.com/bcaf4a0d-8a0d-4016-ab6e-9e1a0fd65d4b">RpcServerUnregisterIf</a>
 

 

