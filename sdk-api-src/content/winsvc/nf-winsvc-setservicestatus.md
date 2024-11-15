---
UID: NF:winsvc.SetServiceStatus
title: SetServiceStatus function (winsvc.h)
description: Updates the service control manager's status information for the calling service.
helpviewer_keywords: ["SetServiceStatus","SetServiceStatus function","_win32_setservicestatus","base.setservicestatus","winsvc/SetServiceStatus"]
old-location: base\setservicestatus.htm
tech.root: security
ms.assetid: bb5943ff-2814-40f2-bee0-ae7132befde9
ms.date: 12/05/2018
ms.keywords: SetServiceStatus, SetServiceStatus function, _win32_setservicestatus, base.setservicestatus, winsvc/SetServiceStatus
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetServiceStatus
 - winsvc/SetServiceStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Service-Core-l1-1-0.dll
 - API-MS-Win-Service-Core-l1-1-1.dll
 - API-Ms-Win-Service-Core-L1-1-2.dll
api_name:
 - SetServiceStatus
---

# SetServiceStatus function


## -description

Updates the service control manager's status information for the calling service.

## -parameters

### -param hServiceStatus [in]

A handle to the status information structure for the current service. This handle is returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa">RegisterServiceCtrlHandlerEx</a> function.

### -param lpServiceStatus [in]

A pointer to the 
<a href="/windows/desktop/api/winsvc/ns-winsvc-service_status">SERVICE_STATUS</a> structure the contains the latest status information for the calling service.

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
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The specified service status structure is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
</table>

## -remarks

A 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> function first calls the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa">RegisterServiceCtrlHandlerEx</a> function to get the service's SERVICE_STATUS_HANDLE. Then it immediately calls the 
<b>SetServiceStatus</b> function to notify the service control manager that its status is SERVICE_START_PENDING. During initialization, the service can provide updated status to indicate that it is making progress but it needs more time. A common bug is for the service to have the main thread perform the initialization while a separate thread continues to call 
<b>SetServiceStatus</b> to prevent the service control manager from marking it as hung. However, if the main thread hangs, then the service start ends up in an infinite loop because the worker thread continues to report that the main thread is making progress.

After processing a control request, the service's 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">Handler</a> function must call 
<b>SetServiceStatus</b> if the service status changes to report its new status to the service control manager. It is only necessary to do so when the service is changing state, such as when it is processing stop or shutdown controls. A service can also use this function at any time from any thread of the service to notify the service control manager of state changes, such as when the service must stop due to a recoverable error.

A service can call this function only after it has called 
<a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa">RegisterServiceCtrlHandlerEx</a> to get a service status handle.

If a service calls 
<b>SetServiceStatus</b> with the <b>dwCurrentState</b> member set to SERVICE_STOPPED and the <b>dwWin32ExitCode</b> member set to a nonzero value, the following entry is written into the System event log:


``` syntax
   Event ID    = 7023
   Source      = Service Control Manager
   Type        = Error
   Description = <ServiceName> terminated with the following error:
                 <ExitCode>.
```

The following are best practices when calling this function:

<ul>
<li>Initialize all fields in the <a href="/windows/desktop/api/winsvc/ns-winsvc-service_status">SERVICE_STATUS</a> structure, ensuring that there are valid check-point and wait hint values for pending states. Use reasonable wait hints.</li>
<li>Do not register to accept controls while the status is SERVICE_START_PENDING or the service can crash. After initialization is completed, accept the SERVICE_CONTROL_STOP code.</li>
<li>Call this function with checkpoint and wait-hint values only if the service is making progress on the tasks related to the pending start, stop, pause, or continue operation. Otherwise, SCM cannot detect if your service is hung.</li>
<li>Enter the stopped state with an appropriate exit code if <a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> fails.</li>
<li>If the status is SERVICE_STOPPED, perform all necessary cleanup and call <b>SetServiceStatus</b> one time only. This function makes an LRPC call to the SCM. The first call to the function in the SERVICE_STOPPED state closes the RPC context handle and any subsequent calls can cause the process to crash. </li>
<li>Do not attempt to perform any additional work after calling <b>SetServiceStatus</b> with SERVICE_STOPPED, because the service process can be terminated at any time.</li>
</ul>

#### Examples

For an example, see 
<a href="/windows/desktop/Services/writing-a-servicemain-function">Writing a ServiceMain Function</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa">RegisterServiceCtrlHandlerEx</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_status">SERVICE_STATUS</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-setservicebits">SetServiceBits</a>
