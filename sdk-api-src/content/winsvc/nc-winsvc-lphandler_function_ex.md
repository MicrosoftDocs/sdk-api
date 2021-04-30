---
UID: NC:winsvc.LPHANDLER_FUNCTION_EX
title: LPHANDLER_FUNCTION_EX (winsvc.h)
description: An application-defined callback function used with the RegisterServiceCtrlHandlerEx function. A service program can use it as the control handler function of a particular service.
helpviewer_keywords: ["HandlerEx","HandlerEx callback","HandlerEx callback function","LPHANDLER_FUNCTION_EX","SERVICE_CONTROL_CONTINUE","SERVICE_CONTROL_DEVICEEVENT","SERVICE_CONTROL_HARDWAREPROFILECHANGE","SERVICE_CONTROL_INTERROGATE","SERVICE_CONTROL_NETBINDADD","SERVICE_CONTROL_NETBINDDISABLE","SERVICE_CONTROL_NETBINDENABLE","SERVICE_CONTROL_NETBINDREMOVE","SERVICE_CONTROL_PARAMCHANGE","SERVICE_CONTROL_PAUSE","SERVICE_CONTROL_POWEREVENT","SERVICE_CONTROL_PRESHUTDOWN","SERVICE_CONTROL_SESSIONCHANGE","SERVICE_CONTROL_SHUTDOWN","SERVICE_CONTROL_STOP","SERVICE_CONTROL_TIMECHANGE","SERVICE_CONTROL_TRIGGEREVENT","SERVICE_CONTROL_USERMODEREBOOT","_win32_handlerex","base.handlerex","winsvc/HandlerEx"]
old-location: base\handlerex.htm
tech.root: security
ms.assetid: bb1b863f-e29f-496f-a50e-9ea524fe8603
ms.date: 12/05/2018
ms.keywords: HandlerEx, HandlerEx callback, HandlerEx callback function, LPHANDLER_FUNCTION_EX, SERVICE_CONTROL_CONTINUE, SERVICE_CONTROL_DEVICEEVENT, SERVICE_CONTROL_HARDWAREPROFILECHANGE, SERVICE_CONTROL_INTERROGATE, SERVICE_CONTROL_NETBINDADD, SERVICE_CONTROL_NETBINDDISABLE, SERVICE_CONTROL_NETBINDENABLE, SERVICE_CONTROL_NETBINDREMOVE, SERVICE_CONTROL_PARAMCHANGE, SERVICE_CONTROL_PAUSE, SERVICE_CONTROL_POWEREVENT, SERVICE_CONTROL_PRESHUTDOWN, SERVICE_CONTROL_SESSIONCHANGE, SERVICE_CONTROL_SHUTDOWN, SERVICE_CONTROL_STOP, SERVICE_CONTROL_TIMECHANGE, SERVICE_CONTROL_TRIGGEREVENT, SERVICE_CONTROL_USERMODEREBOOT, _win32_handlerex, base.handlerex, winsvc/HandlerEx
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPHANDLER_FUNCTION_EX
 - winsvc/LPHANDLER_FUNCTION_EX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WinSvc.h
api_name:
 - HandlerEx
---

# LPHANDLER_FUNCTION_EX callback function


## -description

An application-defined callback function used with the 
    <a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa">RegisterServiceCtrlHandlerEx</a> function. A 
    service program can use it as the control handler function of a particular service.

The <b>LPHANDLER_FUNCTION_EX</b> type defines a pointer to this function. 
    <b>HandlerEx</b> is a placeholder for the application-defined 
    name.

This function supersedes the <a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function">Handler</a> control handler 
    function used with the 
    <a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlera">RegisterServiceCtrlHandler</a> function. A 
    service can use either control handler, but the new control handler supports user-defined context data and 
    additional extended control codes.

## -parameters

### -param dwControl [in]

The control code. This parameter can be one of the following values.

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
Notifies a paused service that it should resume.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_INTERROGATE"></a><a id="service_control_interrogate"></a><dl>
<dt><b>SERVICE_CONTROL_INTERROGATE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Notifies a service to report its current status information to the service control manager.

The handler should simply return <b>NO_ERROR</b>; the SCM is aware of the current state of the service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_NETBINDADD"></a><a id="service_control_netbindadd"></a><dl>
<dt><b>SERVICE_CONTROL_NETBINDADD</b></dt>
<dt>0x00000007</dt>
</dl>
</td>
<td width="60%">
Notifies a network service that there is a new component for binding. The service should bind to the new 
        component. 
        

Applications should use Plug and Play functionality instead.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_NETBINDDISABLE"></a><a id="service_control_netbinddisable"></a><dl>
<dt><b>SERVICE_CONTROL_NETBINDDISABLE</b></dt>
<dt>0x0000000A</dt>
</dl>
</td>
<td width="60%">
Notifies a network service that one of its bindings has been disabled. The service should reread its 
        binding information and remove the binding. 
        

Applications should use Plug and Play functionality instead.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_NETBINDENABLE"></a><a id="service_control_netbindenable"></a><dl>
<dt><b>SERVICE_CONTROL_NETBINDENABLE</b></dt>
<dt>0x00000009</dt>
</dl>
</td>
<td width="60%">
Notifies a network service that a disabled binding has been enabled. The service should reread its 
        binding information and add the new binding. 
        

Applications should use Plug and Play functionality instead.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_NETBINDREMOVE"></a><a id="service_control_netbindremove"></a><dl>
<dt><b>SERVICE_CONTROL_NETBINDREMOVE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Notifies a network service that a component for binding has been removed. The service should reread its 
        binding information and unbind from the removed component. 
        

Applications should use Plug and Play functionality instead.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_PARAMCHANGE"></a><a id="service_control_paramchange"></a><dl>
<dt><b>SERVICE_CONTROL_PARAMCHANGE</b></dt>
<dt>0x00000006</dt>
</dl>
</td>
<td width="60%">
Notifies a service that service-specific startup parameters have changed. The service should reread its 
        startup parameters.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_PAUSE"></a><a id="service_control_pause"></a><dl>
<dt><b>SERVICE_CONTROL_PAUSE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Notifies a service that it should pause.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_PRESHUTDOWN"></a><a id="service_control_preshutdown"></a><dl>
<dt><b>SERVICE_CONTROL_PRESHUTDOWN</b></dt>
<dt>0x0000000F</dt>
</dl>
</td>
<td width="60%">
Notifies a service that the system will be shutting down. Services that need additional time to perform 
        cleanup tasks beyond the tight time restriction at system shutdown can use this notification. The service
        control manager sends this notification to applications that have registered for it before sending a
        <b>SERVICE_CONTROL_SHUTDOWN</b> notification to applications that have registered for that notification.
        

A service that handles this notification blocks system shutdown until the service stops or the preshutdown 
         time-out interval specified through 
         <a href="/windows/desktop/api/winsvc/ns-winsvc-service_preshutdown_info">SERVICE_PRESHUTDOWN_INFO</a> expires. Because 
         this affects the user experience, services should use this feature only if it is absolutely necessary to avoid 
         data loss or significant recovery time at the next system start.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_SHUTDOWN"></a><a id="service_control_shutdown"></a><dl>
<dt><b>SERVICE_CONTROL_SHUTDOWN</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
Notifies a service that the system is shutting down so the service can perform cleanup tasks. Note that 
        services that register for <b>SERVICE_CONTROL_PRESHUTDOWN</b> notifications cannot receive this notification because 
        they have already stopped. 
        

If a service accepts this control code, it must stop after it performs its cleanup tasks and return 
         <b>NO_ERROR</b>. After the SCM sends this control code, it will not send other control codes to the service.

For more information, see the Remarks section of this topic.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_STOP"></a><a id="service_control_stop"></a><dl>
<dt><b>SERVICE_CONTROL_STOP</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Notifies a service that it should stop.
        

If a service accepts this control code, it must stop upon receipt and return <b>NO_ERROR</b>. After the SCM sends 
         this control code, it will not send other control codes to the service.
         <b>Windows XP:  </b>If the service returns <b>NO_ERROR</b> and continues to run, it continues to receive control codes. This 
           behavior changed starting with Windows Server 2003 and Windows XP with SP2.



</td>
</tr>
</table>
 

This parameter can also be one of the following extended control codes. Note that these control codes are not 
       supported by the <a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function">Handler</a> function.

<table>
<tr>
<th>Control Code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_DEVICEEVENT"></a><a id="service_control_deviceevent"></a><dl>
<dt><b>SERVICE_CONTROL_DEVICEEVENT</b></dt>
<dt>0x0000000B</dt>
</dl>
</td>
<td width="60%">
Notifies a service of device events. (The service must have registered to receive these notifications 
        using the <a href="/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa">RegisterDeviceNotification</a> 
        function.) The <i>dwEventType</i> and <i>lpEventData</i> parameters contain additional information.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_HARDWAREPROFILECHANGE"></a><a id="service_control_hardwareprofilechange"></a><dl>
<dt><b>SERVICE_CONTROL_HARDWAREPROFILECHANGE</b></dt>
<dt>0x0000000C</dt>
</dl>
</td>
<td width="60%">
Notifies a service that the computer's hardware profile has changed.  The <i>dwEventType</i> parameter contains additional information.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_POWEREVENT"></a><a id="service_control_powerevent"></a><dl>
<dt><b>SERVICE_CONTROL_POWEREVENT</b></dt>
<dt>0x0000000D</dt>
</dl>
</td>
<td width="60%">
Notifies a service of system power events.  The <i>dwEventType</i> parameter contains additional information. If <i>dwEventType</i> is <a href="/windows/desktop/Power/pbt-powersettingchange">PBT_POWERSETTINGCHANGE</a>, the <i>lpEventData</i> parameter also contains additional information.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_SESSIONCHANGE"></a><a id="service_control_sessionchange"></a><dl>
<dt><b>SERVICE_CONTROL_SESSIONCHANGE</b></dt>
<dt>0x0000000E</dt>
</dl>
</td>
<td width="60%">
Notifies a service of session change events.
        Note that a service will only be notified of a user logon if it is fully loaded before the logon attempt is made.  The <i>dwEventType</i> and <i>lpEventData</i> parameters contain additional information.
      

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_TIMECHANGE"></a><a id="service_control_timechange"></a><dl>
<dt><b>SERVICE_CONTROL_TIMECHANGE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Notifies a service that the system time has changed. The <i>lpEventData</i> parameter contains additional information. The <i>dwEventType</i> parameter is not used.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This control code is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_TRIGGEREVENT"></a><a id="service_control_triggerevent"></a><dl>
<dt><b>SERVICE_CONTROL_TRIGGEREVENT</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Notifies a service registered for a <a href="/windows/desktop/Services/service-trigger-events">service trigger event</a> that the event has occurred. 

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This control code is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_CONTROL_USERMODEREBOOT"></a><a id="service_control_usermodereboot"></a><dl>
<dt><b>SERVICE_CONTROL_USERMODEREBOOT</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Notifies a service that the user has initiated a reboot.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This control code is not supported.

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
<dt>Range 128 to 255.</dt>
</dl>
</td>
<td width="60%">
The service defines the action associated with the control code.

</td>
</tr>
</table>

### -param dwEventType [in]

The type of event that has occurred. This parameter is used if <i>dwControl</i> is 
      <b>SERVICE_CONTROL_DEVICEEVENT</b>, <b>SERVICE_CONTROL_HARDWAREPROFILECHANGE</b>, <b>SERVICE_CONTROL_POWEREVENT</b>, or 
      <b>SERVICE_CONTROL_SESSIONCHANGE</b>. Otherwise, it is zero. 
	     

If <i>dwControl</i> is <b>SERVICE_CONTROL_DEVICEEVENT</b>, this parameter can be one of the 
        following values:

<ul>
<li>
<a href="/windows/desktop/DevIO/dbt-devicearrival">DBT_DEVICEARRIVAL</a>
</li>
<li>
<a href="/windows/desktop/DevIO/dbt-deviceremovecomplete">DBT_DEVICEREMOVECOMPLETE</a>
</li>
<li>
<a href="/windows/desktop/DevIO/dbt-devicequeryremove">DBT_DEVICEQUERYREMOVE</a>
</li>
<li>
<a href="/windows/desktop/DevIO/dbt-devicequeryremovefailed">DBT_DEVICEQUERYREMOVEFAILED</a>
</li>
<li>
<a href="/windows/desktop/DevIO/dbt-deviceremovepending">DBT_DEVICEREMOVEPENDING</a>
</li>
<li>
<a href="/windows/desktop/DevIO/dbt-customevent">DBT_CUSTOMEVENT</a>
</li>
</ul>
If <i>dwControl</i> is <b>SERVICE_CONTROL_HARDWAREPROFILECHANGE</b>, this parameter can be 
        one of the following values:

<ul>
<li>
<a href="/windows/desktop/DevIO/dbt-configchanged">DBT_CONFIGCHANGED</a>
</li>
<li>
<a href="/windows/desktop/DevIO/dbt-querychangeconfig">DBT_QUERYCHANGECONFIG</a>
</li>
<li>
<a href="/windows/desktop/DevIO/dbt-configchangecanceled">DBT_CONFIGCHANGECANCELED</a>
</li>
</ul>
If <i>dwControl</i> is <b>SERVICE_CONTROL_POWEREVENT</b>, this parameter can be one of the values specified in the <i>wParam</i> parameter of the <a href="/windows/desktop/Power/wm-powerbroadcast">WM_POWERBROADCAST</a> message.

If <i>dwControl</i> is <b>SERVICE_CONTROL_SESSIONCHANGE</b>, this parameter can be one of the 
       values specified in the <i>wParam</i> parameter of the 
 	     <a href="/windows/desktop/TermServ/wm-wtssession-change">WM_WTSSESSION_CHANGE</a> message.

### -param lpEventData [in]

Additional device information, if required. The format of this data depends on the value of the 
      <i>dwControl</i> and <i>dwEventType</i> parameters. 

If 
      <i>dwControl</i> is <b>SERVICE_CONTROL_DEVICEEVENT</b>, this data corresponds to the 
      <i>lParam</i> parameter that applications receive as part of a 
      <a href="/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a> message. 

If 
      <i>dwControl</i> is <b>SERVICE_CONTROL_POWEREVENT</b> and <i>dwEventType</i> is PBT_POWERSETTINGCHANGE, this data is a pointer to a 
      <a href="/windows/desktop/api/winuser/ns-winuser-powerbroadcast_setting">POWERBROADCAST_SETTING</a> structure. 

If 
      <i>dwControl</i> is <b>SERVICE_CONTROL_SESSIONCHANGE</b>, this parameter is a pointer to a 
      <a href="/windows/desktop/api/winuser/ns-winuser-wtssession_notification">WTSSESSION_NOTIFICATION</a> 
      structure.

If <i>dwControl</i> is <b>SERVICE_CONTROL_TIMECHANGE</b>, this data is a pointer to a <a href="/windows/desktop/api/winsvc/ns-winsvc-service_timechange_info">SERVICE_TIMECHANGE_INFO</a> structure.

### -param lpContext [in]

User-defined data passed from 
      <a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa">RegisterServiceCtrlHandlerEx</a>.
      When multiple services share a process, the <i>lpContext</i> parameter can help identify the 
      service.

## -returns

The return value for this function depends on the control code received.

The following list identifies the rules for this return value:

<ul>
<li>In general, if your service does not handle the control, return <b>ERROR_CALL_NOT_IMPLEMENTED</b>. However, your service should return <b>NO_ERROR</b> for <b>SERVICE_CONTROL_INTERROGATE</b> even if your service does not handle it.</li>
<li>If your service handles <b>SERVICE_CONTROL_STOP</b> or  <b>SERVICE_CONTROL_SHUTDOWN</b>, return <b>NO_ERROR</b>.</li>
<li>If your service handles <b>SERVICE_CONTROL_DEVICEEVENT</b>, return <b>NO_ERROR</b> to grant the request and an error 
        code to deny the request.</li>
<li>If your service handles <b>SERVICE_CONTROL_HARDWAREPROFILECHANGE</b>, return <b>NO_ERROR</b> to grant the request and 
        an error code to deny the request.</li>
<li>If your service handles <b>SERVICE_CONTROL_POWEREVENT</b>, return <b>NO_ERROR</b> to grant the request and an error 
        code to deny the request.</li>
<li>For all other control codes your service handles, return <b>NO_ERROR</b>.</li>
</ul>

## -remarks

When a service is started, its <a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> function 
    should immediately call the 
    <a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa">RegisterServiceCtrlHandlerEx</a> 
    function to specify a <b>HandlerEx</b> function to process control 
    requests. To specify the control codes to be accepted, use the 
    <a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a> and 
    <a href="/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa">RegisterDeviceNotification</a> functions.

The control dispatcher in the main thread of a service invokes the control handler function for the specified 
    service whenever it receives a control request from the service control manager. After processing the control 
    request, the control handler must call 
    <a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a> if the service state changes to 
    report its new status to the service control manager.

The control handler function is intended to receive notification and return immediately. The 
    callback function should save its parameters and create other threads to perform additional work. (Your application 
    must ensure that such threads have exited before stopping the service.) In particular, a control handler should avoid operations that might block, such as taking a lock, because this could result in a deadlock or cause the system to stop responding.

When the service control manager sends a control code to a service, it waits for the handler function to 
    return before sending additional control codes to other services. The control handler should return as quickly as possible; if it does not return within 30 
    seconds, the SCM returns an error. If a service must do lengthy processing when the service is executing the 
    control handler, it should create a secondary thread to perform the lengthy processing, and then return from the 
    control handler. This prevents the service from tying up the control dispatcher and blocking other services from 
    receiving control codes.

The <b>SERVICE_CONTROL_SHUTDOWN</b> control code should only be processed by services that must absolutely clean up 
    during shutdown, because there is a limited time (about 20 seconds) available for service shutdown. After this 
    time expires, system shutdown proceeds regardless of whether service shutdown is complete. Note that if the system 
    is left in the shutdown state (not restarted or powered down), the service continues to run. If your service registers to accept <b>SERVICE_CONTROL_SHUTDOWN</b>, it must handle the control code and return <b>NO_ERROR</b>. Returning an error for this control code and not stopping in a timely fashion can increase the time required to shut down the system, because the system must wait for the full amount of time allowed for service shutdown before system shutdown can proceed. 

If the service requires more time to clean up, it should send <b>STOP_PENDING</b> status messages, along with a wait 
    hint, so the service controller knows how long to wait before reporting to the system that service shutdown is 
    complete. However, to prevent a service from stopping shutdown, there is a limit to how long the service 
    controller waits. If the service is being shut down through the Services snap-in, the limit is 125 seconds. If the operating system is rebooting, the time limit is specified in the <b>WaitToKillServiceTimeout</b> value of the following registry key:


<b>HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control</b>



Be sure to handle Plug and Play device events as quickly as possible; otherwise, the system may become 
    unresponsive. If your event handler is to perform an operation that may block execution (such as I/O), it is best 
    to start another thread to perform the operation asynchronously.

Services can also use the 
    <a href="/windows/console/setconsolectrlhandler">SetConsoleCtrlHandler</a> function to receive 
    shutdown notification. This notification is received when the running applications are shutting down, which occurs 
    before services are shut down.

## -see-also

<a href="/windows/desktop/api/winuser/ns-winuser-powerbroadcast_setting">POWERBROADCAST_SETTING</a>



<a href="/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa">RegisterDeviceNotification</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa">RegisterServiceCtrlHandlerEx</a>



<a href="/windows/desktop/Services/service-control-handler-function">Service Control Handler Function</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a>



<a href="/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a>



<a href="/windows/desktop/Power/wm-powerbroadcast">WM_POWERBROADCAST</a>



<a href="/windows/desktop/TermServ/wm-wtssession-change">WM_WTSSESSION_CHANGE</a>



<a href="/windows/desktop/api/winuser/ns-winuser-wtssession_notification">WTSSESSION_NOTIFICATION</a>