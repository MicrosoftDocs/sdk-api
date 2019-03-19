---
UID: NF:winsvc.StartServiceW
title: StartServiceW function (winsvc.h)
author: windows-sdk-content
description: Starts a service.
old-location: base\startservice.htm
tech.root: Services
ms.assetid: f185a878-e1c3-4fe5-8ec9-c5296d27f985
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: StartService, StartService function, StartServiceA, StartServiceW, _win32_startservice, base.startservice, winsvc/StartService, winsvc/StartServiceA, winsvc/StartServiceW
ms.topic: function
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StartServiceW (Unicode) and StartServiceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Service-management-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-2-0.dll
api_name:
 - StartService
 - StartServiceA
 - StartServiceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StartServiceW function


## -description


Starts a service.


## -parameters




### -param hService [in]

A handle to the service. This handle is returned by the 
<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a> or 
<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> function, and it must have the SERVICE_START access right. For more information, see 
<a href="https://msdn.microsoft.com/23d1c382-6ba4-49e2-8039-c2a91471076c">Service Security and Access Rights</a>.


### -param dwNumServiceArgs [in]

The number of strings in the <i>lpServiceArgVectors</i> array. If <i>lpServiceArgVectors</i> is NULL, this parameter can be zero.


### -param lpServiceArgVectors [in, optional]

The null-terminated strings to be passed to the <a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a> function for the service as arguments. If there are no arguments, this parameter can be NULL. Otherwise, the first argument (lpServiceArgVectors[0]) is the name of the service, followed by any additional arguments (lpServiceArgVectors[1] through lpServiceArgVectors[dwNumServiceArgs-1]).

Driver services do not receive these arguments.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following error codes can be set by the service control manager. Others can be set by the registry functions that are called by the service control manager.

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
The handle does not have the SERVICE_START access right.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATH_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The service binary file could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_ALREADY_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
An instance of the service is already running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_DATABASE_LOCKED</b></dt>
</dl>
</td>
<td width="60%">
The database is locked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_DEPENDENCY_DELETED</b></dt>
</dl>
</td>
<td width="60%">
The service depends on a service that does not exist or has been marked for deletion.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_DEPENDENCY_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The service depends on another service that has failed to start.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The service has been disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_LOGON_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The service did not start due to a logon failure. This error occurs if the service is configured to run under an account that does not have the "Log on as a service" right.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_MARKED_FOR_DELETE</b></dt>
</dl>
</td>
<td width="60%">
The service has been marked for deletion.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_NO_THREAD</b></dt>
</dl>
</td>
<td width="60%">
A thread could not be created for the service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_REQUEST_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The process for the service was started, but it did not call 
<a href="https://msdn.microsoft.com/8e275eb7-a8af-4bd7-bb39-0eac4f3735ad">StartServiceCtrlDispatcher</a>, or the thread that called 
<b>StartServiceCtrlDispatcher</b> may be blocked in a control handler function.

</td>
</tr>
</table>
 




## -remarks



When a driver service is started, the 
<b>StartService</b> function does not return until the device driver has finished initializing.

When a service is started, the Service Control Manager (SCM) spawns the service process, if necessary. If the specified service shares a process with other services, the required process may already exist. The 
<b>StartService</b> function does not wait for the first status update from the new service, because it can take a while. Instead, it returns when the SCM receives notification from the service control dispatcher that the 
<a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a> thread for this service was created successfully.

The SCM sets the following default status values before returning from 
<b>StartService</b>:

<ul>
<li>Current state of the service is set to SERVICE_START_PENDING.</li>
<li>Controls accepted is set to none (zero).</li>
<li>The CheckPoint value is set to zero.</li>
<li>The WaitHint time is set to 2 seconds.</li>
</ul>
The calling process can determine if the new service has finished its initialization by calling the 
<a href="https://msdn.microsoft.com/dcd2d8a1-10ef-4229-b873-b4fc3ec9293f">QueryServiceStatus</a> function periodically to query the service's status.

A service cannot call 
<b>StartService</b> during initialization. The reason is that the SCM  locks the service control database during initialization, so a call to 
<b>StartService</b> will block. After the service reports to the SCM that it has successfully started, it can call 
<b>StartService</b>.

As with   <a href="https://msdn.microsoft.com/c112b587-7455-4f15-93e1-ded73de6dbbd">ControlService</a>, <b>StartService</b> will block for 30 seconds if any service is busy handling a control code. If the busy service still has not returned from its handler function when the timeout expires,  <b>StartService</b> fails with ERROR_SERVICE_REQUEST_TIMEOUT. This is because the SCM processes only one service control notification at a time.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/7ee5254d-b035-4888-88e9-93e3e55d737e">Starting a Service</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/c112b587-7455-4f15-93e1-ded73de6dbbd">ControlService</a>



<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a>



<a href="https://msdn.microsoft.com/5b0fc714-60e0-4ae3-8fa8-ace36dab2fb0">DeleteService</a>



<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a>



<a href="https://msdn.microsoft.com/499b63fd-e77b-4b90-9ee7-ff4b7b12c431">QueryServiceDynamicInformation</a>



<a href="https://msdn.microsoft.com/3fe02245-97b1-49f3-8f35-2dcd6f221547">QueryServiceStatusEx</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>



<a href="https://msdn.microsoft.com/7d2ee779-1554-436a-a65c-f0322745f46a">Service Startup</a>



<a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a>
 

 

