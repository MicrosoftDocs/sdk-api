---
UID: NF:winsvc.ControlServiceExA
title: ControlServiceExA function (winsvc.h)
description: Sends a control code to a service. (ControlServiceExA)
helpviewer_keywords: ["ControlServiceExA", "SERVICE_CONTROL_CONTINUE", "SERVICE_CONTROL_INTERROGATE", "SERVICE_CONTROL_NETBINDADD", "SERVICE_CONTROL_NETBINDDISABLE", "SERVICE_CONTROL_NETBINDENABLE", "SERVICE_CONTROL_NETBINDREMOVE", "SERVICE_CONTROL_PARAMCHANGE", "SERVICE_CONTROL_PAUSE", "SERVICE_CONTROL_STOP", "winsvc/ControlServiceExA"]
old-location: base\controlserviceex.htm
tech.root: security
ms.assetid: de249903-7545-4fb6-925a-aa647f862f93
ms.date: 12/05/2018
ms.keywords: ControlServiceEx, ControlServiceEx function, ControlServiceExA, ControlServiceExW, SERVICE_CONTROL_CONTINUE, SERVICE_CONTROL_INTERROGATE, SERVICE_CONTROL_NETBINDADD, SERVICE_CONTROL_NETBINDDISABLE, SERVICE_CONTROL_NETBINDENABLE, SERVICE_CONTROL_NETBINDREMOVE, SERVICE_CONTROL_PARAMCHANGE, SERVICE_CONTROL_PAUSE, SERVICE_CONTROL_STOP, base.controlserviceex, winsvc/ControlServiceEx, winsvc/ControlServiceExA, winsvc/ControlServiceExW
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ControlServiceExW (Unicode) and ControlServiceExA (ANSI)
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
 - ControlServiceExA
 - winsvc/ControlServiceExA
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
 - ControlServiceEx
 - ControlServiceExA
 - ControlServiceExW
---

# ControlServiceExA function


## -description

Sends a control code to a service.

## -parameters

### -param hService [in]

A handle to the service. This handle is returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a> or 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function. The 
<a href="/windows/desktop/Services/service-security-and-access-rights">access rights</a> required for this handle depend on the <i>dwControl</i> code requested.

### -param dwControl [in]

This parameter can be one of the following control codes.

<table>
<tr>
<th>Control code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_CONTINUE"></a><a id="service_control_continue"></a><dl>
<dt><b>SERVICE_CONTROL_CONTINUE</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Notifies a paused service that it should resume. The <i>hService</i> handle must have the SERVICE_PAUSE_CONTINUE access right.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_INTERROGATE"></a><a id="service_control_interrogate"></a><dl>
<dt><b>SERVICE_CONTROL_INTERROGATE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Notifies a service that it should report its current status information to the service control manager. The <i>hService</i> handle must have the SERVICE_INTERROGATE access right.

Note that this control is not generally useful as the SCM is aware of the current state of the service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_NETBINDADD"></a><a id="service_control_netbindadd"></a><dl>
<dt><b>SERVICE_CONTROL_NETBINDADD</b></dt>
<dt>0x00000007</dt>
</dl>
</td>
<td width="60%">
 Notifies a network service that there is a new component for binding. The <i>hService</i> handle must have the SERVICE_PAUSE_CONTINUE access right. However,  this control code has been deprecated; use Plug and Play functionality instead.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_NETBINDDISABLE"></a><a id="service_control_netbinddisable"></a><dl>
<dt><b>SERVICE_CONTROL_NETBINDDISABLE</b></dt>
<dt>0x0000000A</dt>
</dl>
</td>
<td width="60%">
 Notifies a network service that one of its bindings has been disabled. The <i>hService</i> handle must have the SERVICE_PAUSE_CONTINUE access right. However,  this control code has been deprecated; use Plug and Play functionality instead.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_NETBINDENABLE"></a><a id="service_control_netbindenable"></a><dl>
<dt><b>SERVICE_CONTROL_NETBINDENABLE</b></dt>
<dt>0x00000009</dt>
</dl>
</td>
<td width="60%">
 Notifies a network service that a disabled binding has been enabled. The <i>hService</i> handle must have the SERVICE_PAUSE_CONTINUE access right. However,  this control code has been deprecated; use Plug and Play functionality instead.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_NETBINDREMOVE"></a><a id="service_control_netbindremove"></a><dl>
<dt><b>SERVICE_CONTROL_NETBINDREMOVE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
 Notifies a network service that a component for binding has been removed. The <i>hService</i> handle must have the SERVICE_PAUSE_CONTINUE access right. However,  this control code has been deprecated; use Plug and Play functionality instead.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_PARAMCHANGE"></a><a id="service_control_paramchange"></a><dl>
<dt><b>SERVICE_CONTROL_PARAMCHANGE</b></dt>
<dt>0x00000006</dt>
</dl>
</td>
<td width="60%">
 Notifies a service that its startup parameters have changed. The <i>hService</i> handle must have the SERVICE_PAUSE_CONTINUE access right.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_PAUSE"></a><a id="service_control_pause"></a><dl>
<dt><b>SERVICE_CONTROL_PAUSE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Notifies a service that it should pause. The <i>hService</i> handle must have the SERVICE_PAUSE_CONTINUE access right.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_STOP"></a><a id="service_control_stop"></a><dl>
<dt><b>SERVICE_CONTROL_STOP</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Notifies a service that it should stop. The <i>hService</i> handle must have the SERVICE_STOP access right.

After sending the stop request to a service, you should not send other controls to the service.

</td>
</tr>
</table>
 

This parameter can also be a user-defined control code, as described in the following table.

<table>
<tr>
<th>Control code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>Range 128 to 255</dt>
</dl>
</td>
<td width="60%">
The service defines the action associated with the control code. The <i>hService</i> handle must have the SERVICE_USER_DEFINED_CONTROL access right.

</td>
</tr>
</table>

### -param dwInfoLevel [in]

The information level for the service control parameters. This parameter must be set to SERVICE_CONTROL_STATUS_REASON_INFO (1).

### -param pControlParams [in, out]

A pointer to the service control parameters. If <i>dwInfoLevel</i> is SERVICE_CONTROL_STATUS_REASON_INFO, this member is a pointer to a <a href="/windows/win32/api/winsvc/ns-winsvc-service_control_status_reason_paramsa">SERVICE_CONTROL_STATUS_REASON_PARAMS</a> structure.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following error codes can be set by the service control manager. Other error codes can be set by the registry functions that are called by the service control manager.

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
The handle does not have the required access right.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DEPENDENT_SERVICES_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The service cannot be stopped because other running services are dependent on it.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle was not obtained using 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> or 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a>, or the handle is no longer valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The requested control code in the <i>dwControl</i> parameter is undefined, or <i>dwControl</i> is SERVICE_CONTROL_STOP but the <b>dwReason</b> or <b>pszComment</b> members of the <a href="/windows/win32/api/winsvc/ns-winsvc-service_control_status_reason_paramsa">SERVICE_CONTROL_STATUS_REASON_PARAMS</a> structure are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SERVICE_CONTROL</b></dt>
</dl>
</td>
<td width="60%">
The requested control code is not valid, or it is unacceptable to the service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_CANNOT_ACCEPT_CTRL</b></dt>
</dl>
</td>
<td width="60%">
The requested control code cannot be sent to the service because the state of the service is SERVICE_STOPPED, SERVICE_START_PENDING, or SERVICE_STOP_PENDING.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_NOT_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The service has not been started.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SHUTDOWN_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The system is shutting down.

</td>
</tr>
</table>

## -remarks

The 
<b>ControlServiceEx</b> function asks the Service Control Manager (SCM) to send the requested control code to the service. The SCM sends the code  if the service has specified that it will accept the code, and is in a state in which a control code can be sent to it.

The SCM processes service control notifications in a serial fashion — it waits for one service to complete processing a service control notification before sending the next one. Because of this, a call to <b>ControlServiceEx</b> blocks for 30 seconds if any service is busy handling a control code. If the busy service still has not returned from its handler function when the timeout expires, <b>ControlServiceEx</b> fails with ERROR_SERVICE_REQUEST_TIMEOUT.

To stop and start a service requires a security descriptor that allows you to do so. The default security descriptor allows the 
<a href="/windows/desktop/Services/localsystem-account">LocalSystem account</a>, and members of the Administrators and Power Users groups to stop and start services. To change the security descriptor of a service, see 
<a href="/windows/desktop/Services/modifying-the-dacl-for-a-service">Modifying the DACL for a Service</a>.

The 
<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex">QueryServiceStatusEx</a> function returns a 
<a href="/windows/desktop/api/winsvc/ns-winsvc-service_status_process">SERVICE_STATUS_PROCESS</a> structure whose <b>dwCurrentState</b> and <b>dwControlsAccepted</b> members indicate the current state and controls accepted by a running service. All running services accept the SERVICE_CONTROL_INTERROGATE control code by default. Drivers do not accept control codes other than SERVICE_CONTROL_STOP and SERVICE_CONTROL_INTERROGATE. Each service specifies the other control codes that it accepts when it calls the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a> function to report its status. A service should always accept these codes when it is running, no matter what it is doing.

The following table shows the action of the SCM  in each of the possible service states.

<table>
<tr>
<th>Service state</th>
<th>Stop</th>
<th>Other controls</th>
</tr>
<tr>
<td>STOPPED</td>
<td>(c)</td>
<td>(c)</td>
</tr>
<tr>
<td>STOP_PENDING</td>
<td>(b)</td>
<td>(b)</td>
</tr>
<tr>
<td>START_PENDING</td>
<td>(a)</td>
<td>(b)</td>
</tr>
<tr>
<td>RUNNING</td>
<td>(a)</td>
<td>(a)</td>
</tr>
<tr>
<td>CONTINUE_PENDING</td>
<td>(a)</td>
<td>(a)</td>
</tr>
<tr>
<td>PAUSE_PENDING</td>
<td>(a)</td>
<td>(a)</td>
</tr>
<tr>
<td>PAUSED</td>
<td>(a)</td>
<td>(a)</td>
</tr>
</table>

<dl>
<dt>(a)</dt>
<dd>
If the service accepts this control code, send the request to the service; otherwise, <b>ControlServiceEx</b> returns
    zero and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns
    <b>ERROR_INVALID_SERVICE_CONTROL</b>.
</dd>
<dt>(b)</dt>
<dd>
The service is not in a state in which a control can be sent to it, so <b>ControlServiceEx</b> returns zero and
    <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns
    <b>ERROR_SERVICE_CANNOT_ACCEPT_CTRL</b>.
</dd>
<dt>(c)</dt>
<dd>
The service is not active, so <b>ControlServiceEx</b> returns zero and
    <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns
    <b>ERROR_SERVICE_NOT_ACTIVE</b>.
</dd>
</dl>


> [!NOTE]
> The winsvc.h header defines ControlServiceEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex">QueryServiceStatusEx</a>



<a href="/windows/win32/api/winsvc/ns-winsvc-service_control_status_reason_paramsa">SERVICE_CONTROL_STATUS_REASON_PARAMS</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_status">SERVICE_STATUS</a>



<a href="/windows/desktop/Services/service-control-requests">Service Control Requests</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity">SetServiceObjectSecurity</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a>
