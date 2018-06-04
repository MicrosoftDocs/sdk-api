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

# OpenNtmsSessionA function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>OpenNtmsSession</b> function sets up a session with a RSM server.


## -parameters




### -param lpServer [in]

RSM server name. If this parameter is <b>NULL</b>, the current computer name is used.


### -param lpApplication [in]

Unique character string that identifies the application. This name identifies resources and operator requests. This parameter is optional and may be <b>NULL</b>.


### -param dwOptions

Reserved; must be zero.


## -returns



If 
<b>OpenNtmsSession</b> succeeds, it returns a handle that uniquely identifies this session. If the function fails, it returns INVALID_HANDLE_VALUE. To retrieve more information, call the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. This function can return one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_COMPUTERNAME</b></dt>
</dl>
</td>
<td width="60%">
The computer name format that was specified was not in a valid format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is not started or not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Unable to connect to the RSM service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
RSM service has not started. The application should wait and retry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INVALID_HANDLE_VALUE</b></dt>
</dl>
</td>
<td width="60%">
RSM cannot open a session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NO_INTERFACES</b></dt>
</dl>
</td>
<td width="60%">
The service is using an older version of RSM than your application.

</td>
</tr>
</table>
 




## -remarks



The 
<b>OpenNtmsSession</b> function returns a session handle used with other RSM functions, establishes a connection with the RSM database, and initializes the RSM subsystem for the application.

When 
<b>OpenNtmsSession</b> returns, the application can perform RSM operations.

Sessions are thread-safe but cannot be passed among processes.




## -see-also




<a href="https://msdn.microsoft.com/54bc354a-fdef-4642-8e53-cf20ed374000">CloseNtmsSession</a>



<a href="removable_storage_manager_functions.htm">Session Management Functions</a>
 

 

