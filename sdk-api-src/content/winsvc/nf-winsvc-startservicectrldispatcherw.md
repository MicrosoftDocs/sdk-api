---
UID: NF:winsvc.StartServiceCtrlDispatcherW
title: StartServiceCtrlDispatcherW function (winsvc.h)
description: Connects the main thread of a service process to the service control manager, which causes the thread to be the service control dispatcher thread for the calling process. (Unicode)
helpviewer_keywords: ["StartServiceCtrlDispatcher", "StartServiceCtrlDispatcher function", "StartServiceCtrlDispatcherW", "_win32_startservicectrldispatcher", "base.startservicectrldispatcher", "winsvc/StartServiceCtrlDispatcher", "winsvc/StartServiceCtrlDispatcherW"]
old-location: base\startservicectrldispatcher.htm
tech.root: security
ms.assetid: 8e275eb7-a8af-4bd7-bb39-0eac4f3735ad
ms.date: 12/05/2018
ms.keywords: StartServiceCtrlDispatcher, StartServiceCtrlDispatcher function, StartServiceCtrlDispatcherA, StartServiceCtrlDispatcherW, _win32_startservicectrldispatcher, base.startservicectrldispatcher, winsvc/StartServiceCtrlDispatcher, winsvc/StartServiceCtrlDispatcherA, winsvc/StartServiceCtrlDispatcherW
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StartServiceCtrlDispatcherW (Unicode) and StartServiceCtrlDispatcherA (ANSI)
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
 - StartServiceCtrlDispatcherW
 - winsvc/StartServiceCtrlDispatcherW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-service-core-l1-1-5.dll
 - api-ms-win-service-core-l1-1-4.dll
 - api-ms-win-service-core-l1-1-3.dll
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Service-Core-l1-1-0.dll
 - API-MS-Win-Service-Core-l1-1-1.dll
 - API-MS-Win-Service-Winsvc-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-2-0.dll
 - API-Ms-Win-Service-Core-L1-1-2.dll
api_name:
 - StartServiceCtrlDispatcher
 - StartServiceCtrlDispatcherA
 - StartServiceCtrlDispatcherW
---

# StartServiceCtrlDispatcherW function


## -description

Connects the main thread of a service process to the service control manager, which causes the thread to be the service control dispatcher thread for the calling process.

## -parameters

### -param lpServiceStartTable [in]

A pointer to an array of 
<a href="/windows/desktop/api/winsvc/ns-winsvc-service_table_entrya">SERVICE_TABLE_ENTRY</a> structures containing one entry for each service that can execute in the calling process. The members of the last entry in the table must have NULL values to designate the end of the table.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following error code can be set by the service control manager. Other error codes can be set by the registry functions that are called by the service control manager.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FAILED_SERVICE_CONTROLLER_CONNECT</b></dt>
</dl>
</td>
<td width="60%">
This error is returned if the program is being run as a console application rather than as a service. 


If the program will be run as a console application for debugging purposes, structure it such that service-specific code is not called when this error is returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The specified dispatch table contains entries that are not in the proper format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_ALREADY_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
 The process has already called 
<a href="/windows/desktop/api/winsvc/nf-winsvc-startservicectrldispatchera">StartServiceCtrlDispatcher</a>. Each process can call 
<b>StartServiceCtrlDispatcher</b> only one time.

</td>
</tr>
</table>

## -remarks

When the service control manager starts a service process, it waits for the process to call the 
<b>StartServiceCtrlDispatcher</b> function. The main thread of a service process should make this call as soon as possible after it starts up (within 30 seconds). If 
<b>StartServiceCtrlDispatcher</b> succeeds, it connects the calling thread to the service control manager and does not return until all running services in the process have entered the SERVICE_STOPPED state. The service control manager uses this connection to send control and service start requests to the main thread of the service process. The main thread acts as a dispatcher by invoking the appropriate 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a> function to handle control requests, or by creating a new thread to execute the appropriate 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> function when a new service is started.

The <i>lpServiceTable</i> parameter contains an entry for each service that can run in the calling process. Each entry specifies the 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> function for that service. For SERVICE_WIN32_SHARE_PROCESS services, each entry must contain the name of a service. This name is the service name that was specified by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function when the service was installed. For SERVICE_WIN32_OWN_PROCESS services, the service name in the table entry is ignored.

If a service runs in its own process, the main thread of the service process should immediately call 
<b>StartServiceCtrlDispatcher</b>. All initialization tasks are done in the service's 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> function when the service is started.

If multiple services share a process and some common process-wide initialization needs to be done before any 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> function is called, the main thread can do the work before calling 
<b>StartServiceCtrlDispatcher</b>, as long as it takes less than 30 seconds. Otherwise, another thread must be created to do the process-wide initialization, while the main thread calls 
<b>StartServiceCtrlDispatcher</b> and becomes the service control dispatcher. Any service-specific initialization should still be done in the individual service main functions.

Services should not attempt to display a user interface directly. For more information, see <a href="/windows/desktop/Services/interactive-services">Interactive Services</a>.


#### Examples

For an example, see 
<a href="/windows/desktop/Services/writing-a-service-program-s-main-function">Writing a Service Program's Main Function</a>.

<div class="code"></div>




> [!NOTE]
> The winsvc.h header defines StartServiceCtrlDispatcher as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-controlservice">ControlService</a>



<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_table_entrya">SERVICE_TABLE_ENTRY</a>



<a href="/windows/desktop/Services/service-entry-point">Service Entry Point</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a>
