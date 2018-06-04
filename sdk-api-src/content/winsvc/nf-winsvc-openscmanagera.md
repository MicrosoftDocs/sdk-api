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

# OpenSCManagerA function


## -description


Establishes a connection to the service control manager on the specified computer and opens the specified service control manager database.


## -parameters




### -param lpMachineName [in, optional]

The name of the target computer. If the pointer is NULL or points to an empty string, the function connects to the service control manager on the local computer.


### -param lpDatabaseName [in, optional]

The name of the service control manager database. This parameter should be set to SERVICES_ACTIVE_DATABASE. If it is NULL, the SERVICES_ACTIVE_DATABASE database is opened by default.


### -param dwDesiredAccess [in]

The access to the service control manager. For a list of access rights, see 
<a href="https://msdn.microsoft.com/23d1c382-6ba4-49e2-8039-c2a91471076c">Service Security and Access Rights</a>. 




Before granting the requested access rights, the system checks the access token of the calling process against the discretionary access-control list of the security descriptor associated with the service control manager.

The SC_MANAGER_CONNECT access right is implicitly specified by calling this function.


## -returns



If the function succeeds, the return value is a handle to the specified service control manager database.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following error codes can be set by the SCM. Other error codes can be set by the registry functions that are called by the SCM.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The requested access was denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The specified database does not exist.

</td>
</tr>
</table>
 




## -remarks



When a process uses the 
<b>OpenSCManager</b> function to open a handle to a service control manager database, the system performs a security check before granting the requested access. For more information, see 
<a href="https://msdn.microsoft.com/23d1c382-6ba4-49e2-8039-c2a91471076c">Service Security and Access Rights</a>.

If the current user does not have proper access when connecting to a service on another computer, the  <b>OpenSCManager</b> function call fails. To connect to a service remotely, call the <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> function with LOGON32_LOGON_NEW_CREDENTIALS and then call <a href="https://msdn.microsoft.com/cf5c31ae-6749-45c2-888f-697060cc8c75">ImpersonateLoggedOnUser</a> before calling <b>OpenSCManager</b>. For more information about connecting to services remotely, see <a href="https://msdn.microsoft.com/c51732f6-c22f-4726-afaa-13a8948ac44f">Services and RPC/TCP</a>.

Only processes with Administrator privileges are able to open a database handle that can be used by the 
<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> function.

The returned handle is only valid for the process that called the 
<b>OpenSCManager</b> function. It can be closed by calling the 
<a href="https://msdn.microsoft.com/6cf25994-4939-4aff-af38-5ffc8fc606ae">CloseServiceHandle</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/79aa4ad5-87ee-4f5d-9c8e-4e788f4c7182">Changing a Service's Configuration</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/6cf25994-4939-4aff-af38-5ffc8fc606ae">CloseServiceHandle</a>



<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a>



<a href="https://msdn.microsoft.com/7d7940c3-b562-455f-9a21-6d5fb5953030">EnumServicesStatusEx</a>



<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a>



<a href="https://msdn.microsoft.com/5ffdd1a9-1a66-4fc4-b35d-4f744bae4897">SCM Handles</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>
 

 

