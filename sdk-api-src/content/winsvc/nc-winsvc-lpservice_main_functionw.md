---
UID: NC:winsvc.LPSERVICE_MAIN_FUNCTIONW
title: LPSERVICE_MAIN_FUNCTIONW (winsvc.h)
description: The entry point for a service. (Unicode)
helpviewer_keywords: ["LPSERVICE_MAIN_FUNCTION","LPSERVICE_MAIN_FUNCTION callback","LPSERVICE_MAIN_FUNCTION callback function","LPSERVICE_MAIN_FUNCTIONA","LPSERVICE_MAIN_FUNCTIONW","ServiceMain","_win32_servicemain","base.servicemain","winsvc/LPSERVICE_MAIN_FUNCTION","winsvc/LPSERVICE_MAIN_FUNCTIONA","winsvc/LPSERVICE_MAIN_FUNCTIONW"]
old-location: base\servicemain.htm
tech.root: security
ms.assetid: d7f3235e-91bd-4107-a30c-4a8f9a6c731e
ms.date: 12/05/2018
ms.keywords: LPSERVICE_MAIN_FUNCTION, LPSERVICE_MAIN_FUNCTION callback, LPSERVICE_MAIN_FUNCTION callback function, LPSERVICE_MAIN_FUNCTIONA, LPSERVICE_MAIN_FUNCTIONW, ServiceMain, _win32_servicemain, base.servicemain, winsvc/LPSERVICE_MAIN_FUNCTION, winsvc/LPSERVICE_MAIN_FUNCTIONA, winsvc/LPSERVICE_MAIN_FUNCTIONW
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
 - LPSERVICE_MAIN_FUNCTIONW
 - winsvc/LPSERVICE_MAIN_FUNCTIONW
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
 - LPSERVICE_MAIN_FUNCTION
 - LPSERVICE_MAIN_FUNCTIONA
 - LPSERVICE_MAIN_FUNCTIONW
---

# LPSERVICE_MAIN_FUNCTIONW callback function


## -description

The entry point for a service.

The <b>LPSERVICE_MAIN_FUNCTION</b> type defines a pointer to this callback function. 
<b>ServiceMain</b> is a placeholder for an application-defined function name.

## -parameters

### -param dwNumServicesArgs [in]

The number of arguments in the <i>lpServiceArgVectors</i> array.

### -param lpServiceArgVectors [in]

The null-terminated argument strings passed to the service by the call to the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-startservicea">StartService</a> function that started the service. If there are no arguments, this parameter can be NULL. Otherwise, the first argument (lpServiceArgVectors[0]) is the name of the service, followed by any additional arguments (lpServiceArgVectors[1] through lpServiceArgVectors[dwNumServicesArgs-1]).

If the user starts a manual service using the Services snap-in from the Control Panel, the strings for the <i>lpServiceArgVectors</i> parameter come from the properties dialog box for the service (from the Services snap-in, right-click the service entry, click <b>Properties</b>, and enter the parameters in <b>Start parameters</b>.)

## -remarks

A service program can start one or more services. A service process has a 
<a href="/windows/desktop/api/winsvc/ns-winsvc-service_table_entrya">SERVICE_TABLE_ENTRY</a> structure for each service that it can start. The structure specifies the service name and a pointer to the 
<b>ServiceMain</b> function for that service.

When the service control manager receives a request to start a service, it starts the service process (if it is not already running). The main thread of the service process calls the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-startservicectrldispatchera">StartServiceCtrlDispatcher</a> function with a pointer to an array of 
<a href="/windows/desktop/api/winsvc/ns-winsvc-service_table_entrya">SERVICE_TABLE_ENTRY</a> structures. Then the service control manager sends a start request to the service control dispatcher for this service process. The service control dispatcher creates a new thread to execute the 
<b>ServiceMain</b> function of the service being started.

The 
<b>ServiceMain</b> function should immediately call the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa">RegisterServiceCtrlHandlerEx</a> function to specify a 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function">HandlerEx</a> function to handle control requests. Next, it should call the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a> function to send status information to the service control manager. After these calls, the function should complete the initialization of the service. Do not attempt to start another service in the 
<b>ServiceMain</b> function.

The Service Control Manager (SCM) waits until the service reports a status of SERVICE_RUNNING. It is recommended that the service reports this status as quickly as possible, as other components in the system that require interaction with SCM will be blocked during this time. Some functions  may require interaction with the SCM either directly or indirectly. 

The SCM locks the service control database during initialization, so if a service attempts to call <a href="/windows/desktop/api/winsvc/nf-winsvc-startservicea">StartService</a> during initialization, the call will block. When the service reports to the SCM that it has successfully started, it can call <b>StartService</b>. If the service requires another service to be running, the service should set the required dependencies.

Furthermore, you should not call any  system functions during service initialization. The service code should call system functions only after it reports a status of SERVICE_RUNNING.

The 
<b>ServiceMain</b> function should create a global event, call the 
<a href="/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject">RegisterWaitForSingleObject</a> function on this event, and exit. This will terminate the thread that is running the 
<b>ServiceMain</b> function, but will not terminate the service. When the service is stopping, the service control handler should call <a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a> with SERVICE_STOP_PENDING and signal this event. A thread from the thread pool will execute the wait callback function; this function should perform clean-up tasks, including closing the global event, and call 
<b>SetServiceStatus</b> with SERVICE_STOPPED. After the service has stopped, you should not execute any additional service code because  you can introduce a race condition if the service receives a start control and <b>ServiceMain</b> is called again. Note that this problem is more likely to occur when multiple services share a process.


#### Examples

For an example, see 
<a href="/windows/desktop/Services/writing-a-servicemain-function">Writing a ServiceMain Function</a>.

<div class="code"></div>

> [!NOTE]
> The winsvc.h header defines LPSERVICE_MAIN_FUNCTION as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa">RegisterServiceCtrlHandlerEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject">RegisterWaitForSingleObject</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_table_entrya">SERVICE_TABLE_ENTRY</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/Services/service-servicemain-function">Service ServiceMain Function</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-startservicectrldispatchera">StartServiceCtrlDispatcher</a>
