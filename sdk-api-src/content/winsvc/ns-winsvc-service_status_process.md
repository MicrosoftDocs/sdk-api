---
UID: NS:winsvc._SERVICE_STATUS_PROCESS
title: SERVICE_STATUS_PROCESS (winsvc.h)
description: Contains process status information for a service. The ControlServiceEx, EnumServicesStatusEx, NotifyServiceStatusChange, and QueryServiceStatusEx functions use this structure.
helpviewer_keywords: ["*LPSERVICE_STATUS_PROCESS","LPSERVICE_STATUS_PROCESS","LPSERVICE_STATUS_PROCESS structure pointer","SERVICE_ACCEPT_HARDWAREPROFILECHANGE","SERVICE_ACCEPT_NETBINDCHANGE","SERVICE_ACCEPT_PARAMCHANGE","SERVICE_ACCEPT_PAUSE_CONTINUE","SERVICE_ACCEPT_POWEREVENT","SERVICE_ACCEPT_PRESHUTDOWN","SERVICE_ACCEPT_SESSIONCHANGE","SERVICE_ACCEPT_SHUTDOWN","SERVICE_ACCEPT_STOP","SERVICE_CONTINUE_PENDING","SERVICE_FILE_SYSTEM_DRIVER","SERVICE_INTERACTIVE_PROCESS","SERVICE_KERNEL_DRIVER","SERVICE_PAUSED","SERVICE_PAUSE_PENDING","SERVICE_RUNNING","SERVICE_RUNS_IN_SYSTEM_PROCESS","SERVICE_START_PENDING","SERVICE_STATUS_PROCESS","SERVICE_STATUS_PROCESS structure","SERVICE_STOPPED","SERVICE_STOP_PENDING","SERVICE_WIN32_OWN_PROCESS","SERVICE_WIN32_SHARE_PROCESS","_win32_service_status_process_str","base.service_status_process_str","winsvc/LPSERVICE_STATUS_PROCESS","winsvc/SERVICE_STATUS_PROCESS"]
old-location: base\service_status_process_str.htm
tech.root: security
ms.assetid: 303986a0-c51e-4078-a3ca-d59e5a302b36
ms.date: 12/05/2018
ms.keywords: '*LPSERVICE_STATUS_PROCESS, LPSERVICE_STATUS_PROCESS, LPSERVICE_STATUS_PROCESS structure pointer, SERVICE_ACCEPT_HARDWAREPROFILECHANGE, SERVICE_ACCEPT_NETBINDCHANGE, SERVICE_ACCEPT_PARAMCHANGE, SERVICE_ACCEPT_PAUSE_CONTINUE, SERVICE_ACCEPT_POWEREVENT, SERVICE_ACCEPT_PRESHUTDOWN, SERVICE_ACCEPT_SESSIONCHANGE, SERVICE_ACCEPT_SHUTDOWN, SERVICE_ACCEPT_STOP, SERVICE_CONTINUE_PENDING, SERVICE_FILE_SYSTEM_DRIVER, SERVICE_INTERACTIVE_PROCESS, SERVICE_KERNEL_DRIVER, SERVICE_PAUSED, SERVICE_PAUSE_PENDING, SERVICE_RUNNING, SERVICE_RUNS_IN_SYSTEM_PROCESS, SERVICE_START_PENDING, SERVICE_STATUS_PROCESS, SERVICE_STATUS_PROCESS structure, SERVICE_STOPPED, SERVICE_STOP_PENDING, SERVICE_WIN32_OWN_PROCESS, SERVICE_WIN32_SHARE_PROCESS, _win32_service_status_process_str, base.service_status_process_str, winsvc/LPSERVICE_STATUS_PROCESS, winsvc/SERVICE_STATUS_PROCESS'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SERVICE_STATUS_PROCESS, *LPSERVICE_STATUS_PROCESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_STATUS_PROCESS
 - winsvc/_SERVICE_STATUS_PROCESS
 - LPSERVICE_STATUS_PROCESS
 - winsvc/LPSERVICE_STATUS_PROCESS
 - SERVICE_STATUS_PROCESS
 - winsvc/SERVICE_STATUS_PROCESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsvc.h
api_name:
 - SERVICE_STATUS_PROCESS
---

# SERVICE_STATUS_PROCESS structure


## -description

Contains process status information for a service. The 
<a href="/windows/desktop/api/winsvc/nf-winsvc-controlserviceexa">ControlServiceEx</a>, <a href="/windows/desktop/api/winsvc/nf-winsvc-enumservicesstatusexa">EnumServicesStatusEx</a>, <a href="/windows/desktop/api/winsvc/nf-winsvc-notifyservicestatuschangea">NotifyServiceStatusChange</a>,  and 
<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex">QueryServiceStatusEx</a> functions use this structure.

## -struct-fields

### -field dwServiceType

The type of service. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_FILE_SYSTEM_DRIVER"></a><a id="service_file_system_driver"></a><dl>
<dt><b>SERVICE_FILE_SYSTEM_DRIVER</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The service is a file system driver.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_KERNEL_DRIVER"></a><a id="service_kernel_driver"></a><dl>
<dt><b>SERVICE_KERNEL_DRIVER</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The service is a device driver.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_WIN32_OWN_PROCESS"></a><a id="service_win32_own_process"></a><dl>
<dt><b>SERVICE_WIN32_OWN_PROCESS</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The service runs in its own process.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_WIN32_SHARE_PROCESS"></a><a id="service_win32_share_process"></a><dl>
<dt><b>SERVICE_WIN32_SHARE_PROCESS</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The service shares a process with other services.

</td>
</tr>
</table>
 

If the service type is either <b>SERVICE_WIN32_OWN_PROCESS</b> or <b>SERVICE_WIN32_SHARE_PROCESS</b>, and the service is running in the context of the 
<a href="/windows/desktop/Services/localsystem-account">LocalSystem account</a>, the following type may also be specified.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_INTERACTIVE_PROCESS"></a><a id="service_interactive_process"></a><dl>
<dt><b>SERVICE_INTERACTIVE_PROCESS</b></dt>
</dl>
</td>
<td width="60%">
The service can interact with the desktop. 




For more information, see 
<a href="/windows/desktop/Services/interactive-services">Interactive Services</a>.

</td>
</tr>
</table>

### -field dwCurrentState

The current state of the service. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTINUE_PENDING"></a><a id="service_continue_pending"></a><dl>
<dt><b>SERVICE_CONTINUE_PENDING</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
The service is about to continue.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_PAUSE_PENDING"></a><a id="service_pause_pending"></a><dl>
<dt><b>SERVICE_PAUSE_PENDING</b></dt>
<dt>0x00000006</dt>
</dl>
</td>
<td width="60%">
The service is pausing.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_PAUSED"></a><a id="service_paused"></a><dl>
<dt><b>SERVICE_PAUSED</b></dt>
<dt>0x00000007</dt>
</dl>
</td>
<td width="60%">
The service is paused.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_RUNNING"></a><a id="service_running"></a><dl>
<dt><b>SERVICE_RUNNING</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The service is running.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_START_PENDING"></a><a id="service_start_pending"></a><dl>
<dt><b>SERVICE_START_PENDING</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The service is starting.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOP_PENDING"></a><a id="service_stop_pending"></a><dl>
<dt><b>SERVICE_STOP_PENDING</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The service is stopping.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_STOPPED"></a><a id="service_stopped"></a><dl>
<dt><b>SERVICE_STOPPED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The service has stopped.

</td>
</tr>
</table>

### -field dwControlsAccepted

The control codes the service accepts and processes in its handler function (see 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function">Handler</a> and 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a>). A user interface process can control a service by specifying a control command in the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-controlservice">ControlService</a> or <a href="/windows/desktop/api/winsvc/nf-winsvc-controlserviceexa">ControlServiceEx</a> function. By default, all services accept the <b>SERVICE_CONTROL_INTERROGATE</b> value. 




The following are the control codes.

<table>
<tr>
<th>Control code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ACCEPT_NETBINDCHANGE"></a><a id="service_accept_netbindchange"></a><dl>
<dt><b>SERVICE_ACCEPT_NETBINDCHANGE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
 The service is a network component that can accept changes in its binding without being stopped and restarted. 




This control code allows the service to receive <b>SERVICE_CONTROL_NETBINDADD</b>, <b>SERVICE_CONTROL_NETBINDREMOVE</b>, <b>SERVICE_CONTROL_NETBINDENABLE</b>, and <b>SERVICE_CONTROL_NETBINDDISABLE</b> notifications.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ACCEPT_PARAMCHANGE"></a><a id="service_accept_paramchange"></a><dl>
<dt><b>SERVICE_ACCEPT_PARAMCHANGE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
 The service can reread its startup parameters without being stopped and restarted. 




This control code allows the service to receive <b>SERVICE_CONTROL_PARAMCHANGE</b> notifications.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ACCEPT_PAUSE_CONTINUE"></a><a id="service_accept_pause_continue"></a><dl>
<dt><b>SERVICE_ACCEPT_PAUSE_CONTINUE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The service can be paused and continued. 




This control code allows the service to receive <b>SERVICE_CONTROL_PAUSE</b> and <b>SERVICE_CONTROL_CONTINUE</b> notifications.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ACCEPT_PRESHUTDOWN"></a><a id="service_accept_preshutdown"></a><dl>
<dt><b>SERVICE_ACCEPT_PRESHUTDOWN</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The service can perform preshutdown tasks. 

This control code enables the service to receive <b>SERVICE_CONTROL_PRESHUTDOWN</b> notifications. Note that 
<a href="/windows/desktop/api/winsvc/nf-winsvc-controlservice">ControlService</a> and <a href="/windows/desktop/api/winsvc/nf-winsvc-controlserviceexa">ControlServiceEx</a> cannot send this notification; only the system can send it.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ACCEPT_SHUTDOWN"></a><a id="service_accept_shutdown"></a><dl>
<dt><b>SERVICE_ACCEPT_SHUTDOWN</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The service is notified when system shutdown occurs. 




This control code allows the service to receive <b>SERVICE_CONTROL_SHUTDOWN</b> notifications. Note that 
<a href="/windows/desktop/api/winsvc/nf-winsvc-controlservice">ControlService</a> and <a href="/windows/desktop/api/winsvc/nf-winsvc-controlserviceexa">ControlServiceEx</a> cannot send this notification; only the system can send it.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ACCEPT_STOP"></a><a id="service_accept_stop"></a><dl>
<dt><b>SERVICE_ACCEPT_STOP</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The service can be stopped. 




This control code allows the service to receive <b>SERVICE_CONTROL_STOP</b> notifications.

</td>
</tr>
</table>
 

This member can also contain the following extended control codes, which are supported only by 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a>. (Note that these control codes cannot be sent by 
<a href="/windows/desktop/api/winsvc/nf-winsvc-controlservice">ControlService</a> or <a href="/windows/desktop/api/winsvc/nf-winsvc-controlserviceexa">ControlServiceEx</a>.)

<table>
<tr>
<th>Control code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ACCEPT_HARDWAREPROFILECHANGE"></a><a id="service_accept_hardwareprofilechange"></a><dl>
<dt><b>SERVICE_ACCEPT_HARDWAREPROFILECHANGE</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
 The service is notified when the computer's hardware profile has changed. This enables the system to send <b>SERVICE_CONTROL_HARDWAREPROFILECHANGE</b> notifications to the service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ACCEPT_POWEREVENT"></a><a id="service_accept_powerevent"></a><dl>
<dt><b>SERVICE_ACCEPT_POWEREVENT</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
 The service is notified when the computer's power status has changed. This enables the system to send <b>SERVICE_CONTROL_POWEREVENT</b> notifications to the service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ACCEPT_SESSIONCHANGE"></a><a id="service_accept_sessionchange"></a><dl>
<dt><b>SERVICE_ACCEPT_SESSIONCHANGE</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
 The service is notified when the computer's session status has changed. This enables the system to send <b>SERVICE_CONTROL_SESSIONCHANGE</b> notifications to the service.

</td>
</tr>
</table>

### -field dwWin32ExitCode

The error code that the service uses to report an error that occurs when it is starting or stopping. To return an error code specific to the service, the service must set this value to <b>ERROR_SERVICE_SPECIFIC_ERROR</b> to indicate that the <b>dwServiceSpecificExitCode</b> member contains the error code. The service should set this value to <b>NO_ERROR</b> when it is running and when it terminates normally.

### -field dwServiceSpecificExitCode

The service-specific error code that the service returns when an error occurs while the service is starting or stopping. This value is ignored unless the <b>dwWin32ExitCode</b> member is set to <b>ERROR_SERVICE_SPECIFIC_ERROR</b>.

### -field dwCheckPoint

The check-point value that the service increments periodically to report its progress during a lengthy start, stop, pause, or continue operation. For example, the service should increment this value as it completes each step of its initialization when it is starting up. The user interface program that invoked the operation on the service uses this value to track the progress of the service during a lengthy operation. This value is not valid and should be zero when the service does not have a start, stop, pause, or continue operation pending.

### -field dwWaitHint

The estimated time required for a pending start, stop, pause, or continue operation, in milliseconds. Before the specified amount of time has elapsed, the service should make its next call to the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a> function with either an incremented <b>dwCheckPoint</b> value or a change in <b>dwCurrentState</b>. If the amount of time specified by <b>dwWaitHint</b> passes, and <b>dwCheckPoint</b> has not been incremented or <b>dwCurrentState</b> has not changed, the service control manager or service control program can assume that an error has occurred and the service should be stopped. However, if the service shares a process with other services, the service control manager cannot terminate the service application because it would have to terminate the other services sharing the process as well.

### -field dwProcessId

The process identifier of the service.

### -field dwServiceFlags

This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The service is running in a process that is not a system process, or it is not running. 




If the service is running in a process that is not a system process, <i>dwProcessId</i> is nonzero. If the service is not running, <i>dwProcessId</i> is zero.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_RUNS_IN_SYSTEM_PROCESS"></a><a id="service_runs_in_system_process"></a><dl>
<dt><b>SERVICE_RUNS_IN_SYSTEM_PROCESS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The service runs in a system process that must always be running.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-controlserviceexa">ControlServiceEx</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-enumservicesstatusexa">EnumServicesStatusEx</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-notifyservicestatuschangea">NotifyServiceStatusChange</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex">QueryServiceStatusEx</a>