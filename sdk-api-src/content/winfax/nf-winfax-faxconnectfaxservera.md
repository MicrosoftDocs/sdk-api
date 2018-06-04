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

# FaxConnectFaxServerA function


## -description


The <b>FaxConnectFaxServer</b> function connects a fax client application to the local fax server. The function returns a fax server handle that is required to call other fax client functions that facilitate job, device, configuration, and document management.


## -parameters




### -param OPTIONAL

TBD


### -param FaxHandle [out]

Type: <b>LPHANDLE</b>

Pointer to a variable that receives a fax server handle that is required on subsequent calls to other fax client functions. If the fax server returns a null handle, it indicates an error.


#### - MachineName [in, optional]

Type: <b>LPCTSTR</b>

This pointer must be <b>NULL</b> (an empty string), so that the application connects to the fax server on the local computer.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. GetLastError can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>FaxHandle</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during memory allocation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user under whose account the call was made does not have sufficient rights to the fax server.

</td>
</tr>
</table>
 




## -remarks



This function can only be used only with a local server. Use of a remote server is enabled in the <a href="https://msdn.microsoft.com/df15bad0-8f68-4eea-9cb3-439078239398">Fax Service Extended COM API</a>. For more information see the <a href="https://msdn.microsoft.com/12e71c4c-c4b5-4e6d-a1fa-b833d6a00ff8">IFaxServer::Connect</a> method.

A fax client application must call the <b>FaxConnectFaxServer</b> function successfully before it calls any other fax client function.

The fax client application must call the <a href="https://msdn.microsoft.com/d2a59e30-24bd-4a65-ba9b-8187ed6f53f6">FaxClose</a> function to disconnect from the fax server and deallocate the handle that the <b>FaxConnectFaxServer</b> function returns. For more information, see <a href="https://msdn.microsoft.com/aa3cd5cf-fff5-453b-9574-7ef617239da6">Connecting to the Fax Server</a> and <a href="https://msdn.microsoft.com/02d276b7-bcbc-4bbe-8051-d9b35f12dc93">Disconnecting from a Fax Server</a>.




## -see-also




<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/d2a59e30-24bd-4a65-ba9b-8187ed6f53f6">FaxClose</a>
 

 

