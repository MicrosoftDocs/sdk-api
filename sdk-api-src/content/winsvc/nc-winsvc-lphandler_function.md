---
UID: NC:winsvc.LPHANDLER_FUNCTION
title: LPHANDLER_FUNCTION (winsvc.h)
description: An application-defined callback function used with the RegisterServiceCtrlHandler function. A service program can use it as the control handler function of a particular service.
helpviewer_keywords: ["Handler","Handler callback","Handler callback function","LPHANDLER_FUNCTION","SERVICE_CONTROL_CONTINUE","SERVICE_CONTROL_INTERROGATE","SERVICE_CONTROL_NETBINDADD","SERVICE_CONTROL_NETBINDDISABLE","SERVICE_CONTROL_NETBINDENABLE","SERVICE_CONTROL_NETBINDREMOVE","SERVICE_CONTROL_PARAMCHANGE","SERVICE_CONTROL_PAUSE","SERVICE_CONTROL_SHUTDOWN","SERVICE_CONTROL_STOP","_win32_handler","base.handler","winsvc/Handler"]
old-location: base\handler.htm
tech.root: security
ms.assetid: e2d6d3a7-070e-4343-abd7-b4b9f8dd6fbc
ms.date: 12/05/2018
ms.keywords: Handler, Handler callback, Handler callback function, LPHANDLER_FUNCTION, SERVICE_CONTROL_CONTINUE, SERVICE_CONTROL_INTERROGATE, SERVICE_CONTROL_NETBINDADD, SERVICE_CONTROL_NETBINDDISABLE, SERVICE_CONTROL_NETBINDENABLE, SERVICE_CONTROL_NETBINDREMOVE, SERVICE_CONTROL_PARAMCHANGE, SERVICE_CONTROL_PAUSE, SERVICE_CONTROL_SHUTDOWN, SERVICE_CONTROL_STOP, _win32_handler, base.handler, winsvc/Handler
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
 - LPHANDLER_FUNCTION
 - winsvc/LPHANDLER_FUNCTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winsvc.h
api_name:
 - Handler
---

# LPHANDLER_FUNCTION callback function


## -description

An application-defined callback function used with the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlera">RegisterServiceCtrlHandler</a> function. A service program can use it as the control handler function of a particular service.

The <b>LPHANDLER_FUNCTION</b> type defines a pointer to this function. 
<b>Handler</b> is a placeholder for the application-defined name.

This function has been superseded by the 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a> control handler function used with the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa">RegisterServiceCtrlHandlerEx</a> function. A service can use either control handler, but the new control handler supports user-defined context data and additional extended control codes.

## -parameters

### -param dwControl

#### - fdwControl [in]

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
Notifies a service that it should report its current status information to the service control manager.

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
 Notifies a network service that there is a new component for binding. The service should bind to the new component. 

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
 Notifies a network service that one of its bindings has been disabled. The service should reread its binding information and remove the binding. 

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
 Notifies a network service that a disabled binding has been enabled. The service should reread its binding information and add the new binding. 

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
 Notifies a network service that a component for binding has been removed. The service should reread its binding information and unbind from the removed component. 

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
 Notifies a service that its startup parameters have changed. The service should reread its startup parameters.

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
<td width="40%"><a id="SERVICE_CONTROL_SHUTDOWN"></a><a id="service_control_shutdown"></a><dl>
<dt><b>SERVICE_CONTROL_SHUTDOWN</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
Notifies a service that the system is shutting down so the service can perform cleanup tasks. 




If a service accepts this control code, it must stop after it performs its cleanup tasks and return <b>NO_ERROR</b>. After the SCM sends this control code, it will not send other control codes to the service.

For more information, see Remarks.

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

If a service accepts this control code, it must stop upon receipt and return <b>NO_ERROR</b>. After the SCM sends this control code, it does not send other control codes.<b>Windows XP:  </b>If the service returns <b>NO_ERROR</b> and continues to run, it   continues to receive control codes. This behavior changed starting with Windows Server 2003 and Windows XP with SP2.



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

## -remarks

When a service is started, its 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> function should immediately call the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlera">RegisterServiceCtrlHandler</a> function to specify a 
<b>Handler</b> function to process control requests.

The control dispatcher in the main thread of a service process invokes the control handler function for the specified service whenever it receives a control request from the service control manager. After processing the control request, the control handler must call the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a> function if the service state changes to report its new status to the service control manager.

The control handler function is intended to receive notification and return immediately. The callback function should save its parameters and create other threads to perform additional work. (Your application must ensure that such threads have exited before stopping the service.) In particular, a control handler should avoid  operations that might block, such as taking a lock, because this could result  in  a deadlock or cause the system to stop responding. 

When the service control manager sends a control code to a service, it waits for the handler function to return before sending additional control codes to other services. The control handler should return as quickly as possible; if it does not return within 30 seconds, the SCM  returns an error. If a service must do lengthy processing when the service is executing the control handler, it should create a secondary thread to perform the lengthy processing, and then return from the control handler. This prevents the service from tying up the control dispatcher and blocking other services from receiving control codes.

The <b>SERVICE_CONTROL_SHUTDOWN</b> control code should only be processed by services that must absolutely clean up during shutdown, because there is a limited time (about 20 seconds) available for service shutdown. After this time expires, system shutdown proceeds regardless of whether service shutdown is complete. Note that if the system is left in the shutdown state (not restarted or powered down), the service continues to run.   If your service registers to accept <b>SERVICE_CONTROL_SHUTDOWN</b>, it must handle the control code and stop  in a timely fashion. Otherwise, the service can increase the time required to shut down the system, because the system must wait for the full amount of time allowed for service shutdown before system shutdown can proceed. 

If the service requires more time to clean up, it should send <b>STOP_PENDING</b> status messages, along with a wait hint, so the service controller knows how long to wait before reporting to the system that service shutdown is complete. However, to prevent a service from stopping shutdown, there is a limit to how long the service controller will wait. If the service is being shut down through the Services snap-in, the limit is 125 seconds. If the operating system is rebooting, the time limit is specified in the <b>WaitToKillServiceTimeout</b> value of the following registry key:


<b>HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control</b>



Services can also use the <a href="/windows/console/setconsolectrlhandler">SetConsoleCtrlHandler</a> function to receive shutdown notification. This notification is received when the running applications are shutting down, which occurs before services are shut down.


#### Examples

For an example, see 
<a href="/windows/desktop/Services/writing-a-control-handler-function">Writing a Control Handler Function</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlera">RegisterServiceCtrlHandler</a>



<a href="/windows/desktop/Services/service-control-handler-function">Service Control Handler Function</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a>