---
UID: NF:winsvc.ControlService
title: ControlService function (winsvc.h)
description: Sends a control code to a service. (ControlService)
helpviewer_keywords: ["ControlService","ControlService function","SERVICE_CONTROL_CONTINUE","SERVICE_CONTROL_INTERROGATE","SERVICE_CONTROL_NETBINDADD","SERVICE_CONTROL_NETBINDDISABLE","SERVICE_CONTROL_NETBINDENABLE","SERVICE_CONTROL_NETBINDREMOVE","SERVICE_CONTROL_PARAMCHANGE","SERVICE_CONTROL_PAUSE","SERVICE_CONTROL_STOP","_win32_controlservice","base.controlservice","winsvc/ControlService"]
old-location: base\controlservice.htm
tech.root: security
ms.assetid: c112b587-7455-4f15-93e1-ded73de6dbbd
ms.date: 12/05/2018
ms.keywords: ControlService, ControlService function, SERVICE_CONTROL_CONTINUE, SERVICE_CONTROL_INTERROGATE, SERVICE_CONTROL_NETBINDADD, SERVICE_CONTROL_NETBINDDISABLE, SERVICE_CONTROL_NETBINDENABLE, SERVICE_CONTROL_NETBINDREMOVE, SERVICE_CONTROL_PARAMCHANGE, SERVICE_CONTROL_PAUSE, SERVICE_CONTROL_STOP, _win32_controlservice, base.controlservice, winsvc/ControlService
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: AdvApi32.lib
req.dll: AdvApi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ControlService
 - winsvc/ControlService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - AdvApi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Service-Winsvc-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-2-0.dll
api_name:
 - ControlService
---

# ControlService function


## -description

Sends a control code to a service.

To specify additional information when stopping a service, use the 
    <a href="/windows/desktop/api/winsvc/nf-winsvc-controlserviceexa">ControlServiceEx</a> function.

## -parameters

### -param hService [in]

A handle to the service. This handle is returned by the 
      <a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a> or 
      <a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function. The 
      <a href="/windows/desktop/Services/service-security-and-access-rights">access rights</a> required for this handle 
      depend on the <i>dwControl</i> code requested.

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
Notifies a paused service that it should resume. The <i>hService</i> handle must have 
        the <b>SERVICE_PAUSE_CONTINUE</b> access right.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_INTERROGATE"></a><a id="service_control_interrogate"></a><dl>
<dt><b>SERVICE_CONTROL_INTERROGATE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Notifies a service that it should report its current status information to the service control manager. 
        The <i>hService</i> handle must have the <b>SERVICE_INTERROGATE</b> 
        access right.
        

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
Notifies a network service that there is a new component for binding. The 
        <i>hService</i> handle must have the <b>SERVICE_PAUSE_CONTINUE</b> 
        access right. However, this control code has been deprecated; use Plug and Play functionality instead.
        
       

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_NETBINDDISABLE"></a><a id="service_control_netbinddisable"></a><dl>
<dt><b>SERVICE_CONTROL_NETBINDDISABLE</b></dt>
<dt>0x0000000A</dt>
</dl>
</td>
<td width="60%">
Notifies a network service that one of its bindings has been disabled. The 
        <i>hService</i> handle must have the <b>SERVICE_PAUSE_CONTINUE</b> 
        access right. However, this control code has been deprecated; use Plug and Play functionality instead.
        
       

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_NETBINDENABLE"></a><a id="service_control_netbindenable"></a><dl>
<dt><b>SERVICE_CONTROL_NETBINDENABLE</b></dt>
<dt>0x00000009</dt>
</dl>
</td>
<td width="60%">
Notifies a network service that a disabled binding has been enabled. The 
        <i>hService</i> handle must have the <b>SERVICE_PAUSE_CONTINUE</b> 
        access right. However, this control code has been deprecated; use Plug and Play functionality instead.
        
       

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_NETBINDREMOVE"></a><a id="service_control_netbindremove"></a><dl>
<dt><b>SERVICE_CONTROL_NETBINDREMOVE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
 Notifies a network service that a component for binding has been removed. The 
        <i>hService</i> handle must have the <b>SERVICE_PAUSE_CONTINUE</b> 
        access right. However, this control code has been deprecated; use Plug and Play functionality instead.
        
       

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_PARAMCHANGE"></a><a id="service_control_paramchange"></a><dl>
<dt><b>SERVICE_CONTROL_PARAMCHANGE</b></dt>
<dt>0x00000006</dt>
</dl>
</td>
<td width="60%">
Notifies a service that its startup parameters have changed. The <i>hService</i> 
        handle must have the <b>SERVICE_PAUSE_CONTINUE</b> access right.
        
       

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_PAUSE"></a><a id="service_control_pause"></a><dl>
<dt><b>SERVICE_CONTROL_PAUSE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Notifies a service that it should pause. The <i>hService</i> handle must have the 
        <b>SERVICE_PAUSE_CONTINUE</b> access right.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_STOP"></a><a id="service_control_stop"></a><dl>
<dt><b>SERVICE_CONTROL_STOP</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Notifies a service that it should stop. The <i>hService</i> handle must have the 
        <b>SERVICE_STOP</b> access right.
        

After sending the stop request to a service, you should not send other controls to the service.

</td>
</tr>
</table>
 

This value can also be a user-defined control code, as described in the following table.

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
The service defines the action associated with the control code. The <i>hService</i> 
        handle must have the <b>SERVICE_USER_DEFINED_CONTROL</b> access right.

</td>
</tr>
</table>

### -param lpServiceStatus [out]

A pointer to a <a href="/windows/desktop/api/winsvc/ns-winsvc-service_status">SERVICE_STATUS</a> structure that 
      receives the latest service status information. The information returned reflects the most recent status that 
      the service reported to the service control manager.
      

The service control manager fills in the structure only when 
       [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns one of the following error 
       codes: <b>NO_ERROR</b>, <b>ERROR_INVALID_SERVICE_CONTROL</b>, 
       <b>ERROR_SERVICE_CANNOT_ACCEPT_CTRL</b>, or 
       <b>ERROR_SERVICE_NOT_ACTIVE</b>. Otherwise, the structure is not filled in.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following error codes can be set by the service control manager. Other error codes can be set by the 
       registry functions that are called by the service control manager.

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
        <a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a>, or the handle is no longer 
        valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The requested control code is undefined.

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
The requested control code cannot be sent to the service because the state of the service is 
        <b>SERVICE_STOPPED</b>, <b>SERVICE_START_PENDING</b>, or 
        <b>SERVICE_STOP_PENDING</b>.

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
        <a href="/windows/desktop/api/winsvc/nf-winsvc-startservicectrldispatchera">StartServiceCtrlDispatcher</a>, or the 
        thread that called 
        <b>StartServiceCtrlDispatcher</b> may be 
        blocked in a control handler function.

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

The <b>ControlService</b> function asks the Service 
    Control Manager (SCM) to send the requested control code to the service. The SCM sends the code  if the service 
    has specified that it will accept the code, and is in a state in which a control code can be sent to it.

The SCM processes service control notifications in a serial fashion—it will wait for one 
    service to complete processing a service control notification before sending the next one. Because of this, a call 
    to <b>ControlService</b> will block for 30 seconds if any 
    service is busy handling a control code. If the busy service still has not returned from its handler function when 
    the timeout expires, <b>ControlService</b> fails with 
    <b>ERROR_SERVICE_REQUEST_TIMEOUT</b>.

To stop and start a service requires a security descriptor that allows you to do so. The default security 
    descriptor allows the <a href="/windows/desktop/Services/localsystem-account">LocalSystem account</a>, and members 
    of the Administrators and Power Users groups to stop and start services. To change the security descriptor of a 
    service, see 
    <a href="/windows/desktop/Services/modifying-the-dacl-for-a-service">Modifying the DACL for a Service</a>.

The <a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex">QueryServiceStatusEx</a> function returns a 
    <a href="/windows/desktop/api/winsvc/ns-winsvc-service_status_process">SERVICE_STATUS_PROCESS</a> structure 
    whose <b>dwCurrentState</b> and <b>dwControlsAccepted</b> members indicate 
    the current state and controls accepted by a running service. All running services accept the 
    <b>SERVICE_CONTROL_INTERROGATE</b> control code by default. Drivers do not accept control codes 
    other than <b>SERVICE_CONTROL_STOP</b> and 
    <b>SERVICE_CONTROL_INTERROGATE</b>. Each service specifies the other control codes that it 
    accepts when it calls the <a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a> function 
    to report its status. A service should always accept these codes when it is running, no matter what it is 
    doing.

The following table shows the action of the SCM  in each of the possible service states.

<table>
<tr>
<th>Service state</th>
<th>Stop</th>
<th>Other controls</th>
</tr>
<tr>
<td><b>STOPPED</b></td>
<td>(c)</td>
<td>(c)</td>
</tr>
<tr>
<td><b>STOP_PENDING</b></td>
<td>(b)</td>
<td>(b)</td>
</tr>
<tr>
<td><b>START_PENDING</b></td>
<td>(a)</td>
<td>(b)</td>
</tr>
<tr>
<td><b>RUNNING</b></td>
<td>(a)</td>
<td>(a)</td>
</tr>
<tr>
<td><b>CONTINUE_PENDING</b></td>
<td>(a)</td>
<td>(a)</td>
</tr>
<tr>
<td><b>PAUSE_PENDING</b></td>
<td>(a)</td>
<td>(a)</td>
</tr>
<tr>
<td><b>PAUSED</b></td>
<td>(a)</td>
<td>(a)</td>
</tr>
</table>

<dl>
<dt>(a)</dt>
<dd>
If the service accepts this control code, send the request to the service; otherwise, <b>ControlService</b> returns zero
    and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns
    <b>ERROR_INVALID_SERVICE_CONTROL</b>.
</dd>
<dt>(b)</dt>
<dd>
The service is not in a state in which a control can be sent to it, so <b>ControlService</b> returns zero and
    <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns
    <b>ERROR_SERVICE_CANNOT_ACCEPT_CTRL</b>.
</dd>
<dt>(c)</dt>
<dd>
The service is not active, so <b>ControlService</b> returns zero and
    <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns
    <b>ERROR_SERVICE_NOT_ACTIVE</b>.
</dd>
</dl>


#### Examples

For an example, see <a href="/windows/desktop/Services/stopping-a-service">Stopping a Service</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-controlserviceexa">ControlServiceEx</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex">QueryServiceStatusEx</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_status">SERVICE_STATUS</a>



<a href="/windows/desktop/Services/service-control-requests">Service Control Requests</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity">SetServiceObjectSecurity</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a>
