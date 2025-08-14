---
UID: NF:winsvc.StartServiceW
title: StartServiceW function (winsvc.h)
description: Starts a service. (Unicode)
helpviewer_keywords: ["StartService", "StartService function", "StartServiceW", "_win32_startservice", "base.startservice", "winsvc/StartService", "winsvc/StartServiceW"]
old-location: base\startservice.htm
tech.root: security
ms.assetid: f185a878-e1c3-4fe5-8ec9-c5296d27f985
ms.date: 12/05/2018
ms.keywords: StartService, StartService function, StartServiceA, StartServiceW, _win32_startservice, base.startservice, winsvc/StartService, winsvc/StartServiceA, winsvc/StartServiceW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StartServiceW
 - winsvc/StartServiceW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
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
---

# StartServiceW function


## -description

Starts a service.

## -parameters

### -param hService [in]

A handle to the service. This handle is returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a> or 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function, and it must have the SERVICE_START access right. For more information, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>.

### -param dwNumServiceArgs [in]

The number of strings in the <i>lpServiceArgVectors</i> array. If <i>lpServiceArgVectors</i> is NULL, this parameter can be zero.

### -param lpServiceArgVectors [in, optional]

The null-terminated strings to be passed to the <a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> function for the service as arguments. If there are no arguments, this parameter can be NULL. Otherwise, the first argument (lpServiceArgVectors[0]) is the name of the service, followed by any additional arguments (lpServiceArgVectors[1] through lpServiceArgVectors[dwNumServiceArgs-1]).

Driver services do not receive these arguments.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

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
<a href="/windows/desktop/api/winsvc/nf-winsvc-startservicectrldispatchera">StartServiceCtrlDispatcher</a>, or the thread that called 
<b>StartServiceCtrlDispatcher</b> may be blocked in a control handler function.

</td>
</tr>
</table>

## -remarks

When a driver service is started, the 
<b>StartService</b> function does not return until the device driver has finished initializing.

When a service is started, the Service Control Manager (SCM) spawns the service process, if necessary. If the specified service shares a process with other services, the required process may already exist. The 
<b>StartService</b> function does not wait for the first status update from the new service, because it can take a while. Instead, it returns when the SCM receives notification from the service control dispatcher that the 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> thread for this service was created successfully.

The SCM sets the following default status values before returning from 
<b>StartService</b>:

<ul>
<li>Current state of the service is set to SERVICE_START_PENDING.</li>
<li>Controls accepted is set to none (zero).</li>
<li>The CheckPoint value is set to zero.</li>
<li>The WaitHint time is set to 2 seconds.</li>
</ul>
The calling process can determine if the new service has finished its initialization by calling the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicestatus">QueryServiceStatus</a> function periodically to query the service's status.

A service cannot call 
<b>StartService</b> during initialization. The reason is that the SCM  locks the service control database during initialization, so a call to 
<b>StartService</b> will block. After the service reports to the SCM that it has successfully started, it can call 
<b>StartService</b>.

As with   <a href="/windows/desktop/api/winsvc/nf-winsvc-controlservice">ControlService</a>, <b>StartService</b> will block for 30 seconds if any service is busy handling a control code. If the busy service still has not returned from its handler function when the timeout expires,  <b>StartService</b> fails with ERROR_SERVICE_REQUEST_TIMEOUT. This is because the SCM processes only one service control notification at a time.


#### Examples

For an example, see 
<a href="/windows/desktop/Services/starting-a-service">Starting a Service</a>.

<div class="code"></div>




> [!NOTE]
> The winsvc.h header defines StartService as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-controlservice">ControlService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-deleteservice">DeleteService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicedynamicinformation">QueryServiceDynamicInformation</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex">QueryServiceStatusEx</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/Services/service-startup">Service Startup</a>



<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a>
