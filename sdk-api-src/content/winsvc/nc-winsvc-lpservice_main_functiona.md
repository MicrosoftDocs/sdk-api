---
UID: NC:winsvc.LPSERVICE_MAIN_FUNCTIONA
title: LPSERVICE_MAIN_FUNCTIONA (winsvc.h)
author: windows-sdk-content
description: The entry point for a service.
old-location: base\servicemain.htm
tech.root: Services
ms.assetid: d7f3235e-91bd-4107-a30c-4a8f9a6c731e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LPSERVICE_MAIN_FUNCTION, LPSERVICE_MAIN_FUNCTION callback, LPSERVICE_MAIN_FUNCTION callback function, LPSERVICE_MAIN_FUNCTIONA, LPSERVICE_MAIN_FUNCTIONW, ServiceMain, _win32_servicemain, base.servicemain, winsvc/LPSERVICE_MAIN_FUNCTION, winsvc/LPSERVICE_MAIN_FUNCTIONA, winsvc/LPSERVICE_MAIN_FUNCTIONW
ms.topic: callback
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LPSERVICE_MAIN_FUNCTIONA callback function


## -description


The entry point for a service.

The <b>LPSERVICE_MAIN_FUNCTION</b> type defines a pointer to this callback function. 
<b>ServiceMain</b> is a placeholder for an application-defined function name.


## -parameters




### -param dwNumServicesArgs


### -param *lpServiceArgVectors








#### - dwArgc [in]

The number of arguments in the <i>lpszArgv</i> array.


#### - lpszArgv [in]

The null-terminated argument strings passed to the service by the call to  the 
<a href="https://msdn.microsoft.com/f185a878-e1c3-4fe5-8ec9-c5296d27f985">StartService</a> function that started the service. If there are no arguments, this parameter can be NULL. Otherwise, the first argument (lpszArgv[0]) is the name of the service, followed by any additional arguments (lpszArgv[1] through lpszArgv[dwArgc-1]).

If the user starts a manual service using the Services snap-in from the Control Panel, the strings for the <i>lpszArgv</i> parameter come from the properties dialog box for the service (from the Services snap-in, right-click the service entry, click <b>Properties</b>, and enter the parameters in <b>Start parameters</b>.)


## -returns



This function does not return a value.




## -remarks



A service program can start one or more services. A service process has a 
<a href="https://msdn.microsoft.com/dd40c4f0-cbbe-429f-91c0-3ba141dab702">SERVICE_TABLE_ENTRY</a> structure for each service that it can start. The structure specifies the service name and a pointer to the 
<b>ServiceMain</b> function for that service.

When the service control manager receives a request to start a service, it starts the service process (if it is not already running). The main thread of the service process calls the 
<a href="https://msdn.microsoft.com/8e275eb7-a8af-4bd7-bb39-0eac4f3735ad">StartServiceCtrlDispatcher</a> function with a pointer to an array of 
<a href="https://msdn.microsoft.com/dd40c4f0-cbbe-429f-91c0-3ba141dab702">SERVICE_TABLE_ENTRY</a> structures. Then the service control manager sends a start request to the service control dispatcher for this service process. The service control dispatcher creates a new thread to execute the 
<b>ServiceMain</b> function of the service being started.

The 
<b>ServiceMain</b> function should immediately call the 
<a href="https://msdn.microsoft.com/23eea346-9899-4214-88f4-9b7eb7ce1332">RegisterServiceCtrlHandlerEx</a> function to specify a 
<a href="https://msdn.microsoft.com/e2d6d3a7-070e-4343-abd7-b4b9f8dd6fbc">HandlerEx</a> function to handle control requests. Next, it should call the 
<a href="https://msdn.microsoft.com/bb5943ff-2814-40f2-bee0-ae7132befde9">SetServiceStatus</a> function to send status information to the service control manager. After these calls, the function should complete the initialization of the service. Do not attempt to start another service in the 
<b>ServiceMain</b> function.

The Service Control Manager (SCM) waits until the service reports a status of SERVICE_RUNNING. It is recommended that the service reports this status as quickly as possible, as other components in the system that require interaction with SCM will be blocked during this time. Some functions  may require interaction with the SCM either directly or indirectly. 

The SCM locks the service control database during initialization, so if a service attempts to call <a href="https://msdn.microsoft.com/f185a878-e1c3-4fe5-8ec9-c5296d27f985">StartService</a> during initialization, the call will block. When the service reports to the SCM that it has successfully started, it can call <b>StartService</b>. If the service requires another service to be running, the service should set the required dependencies.

Furthermore, you should not call any  system functions during service initialization. The service code should call system functions only after it reports a status of SERVICE_RUNNING.

The 
<b>ServiceMain</b> function should create a global event, call the 
<a href="https://msdn.microsoft.com/d0cd8b28-6e20-449a-94dd-cca2be46b812">RegisterWaitForSingleObject</a> function on this event, and exit. This will terminate the thread that is running the 
<b>ServiceMain</b> function, but will not terminate the service. When the service is stopping, the service control handler should call <a href="https://msdn.microsoft.com/bb5943ff-2814-40f2-bee0-ae7132befde9">SetServiceStatus</a> with SERVICE_STOP_PENDING and signal this event. A thread from the thread pool will execute the wait callback function; this function should perform clean-up tasks, including closing the global event, and call 
<b>SetServiceStatus</b> with SERVICE_STOPPED. After the service has stopped, you should not execute any additional service code because  you can introduce a race condition if the service receives a start control and <b>ServiceMain</b> is called again. Note that this problem is more likely to occur when multiple services share a process.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/7aa9371d-676c-4633-9831-edf0e74d15f0">Writing a ServiceMain Function</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/bb1b863f-e29f-496f-a50e-9ea524fe8603">HandlerEx</a>



<a href="https://msdn.microsoft.com/23eea346-9899-4214-88f4-9b7eb7ce1332">RegisterServiceCtrlHandlerEx</a>



<a href="https://msdn.microsoft.com/d0cd8b28-6e20-449a-94dd-cca2be46b812">RegisterWaitForSingleObject</a>



<a href="https://msdn.microsoft.com/dd40c4f0-cbbe-429f-91c0-3ba141dab702">SERVICE_TABLE_ENTRY</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>



<a href="https://msdn.microsoft.com/e55e056f-7628-4e3d-9aea-b55c371b4287">Service ServiceMain Function</a>



<a href="https://msdn.microsoft.com/bb5943ff-2814-40f2-bee0-ae7132befde9">SetServiceStatus</a>



<a href="https://msdn.microsoft.com/8e275eb7-a8af-4bd7-bb39-0eac4f3735ad">StartServiceCtrlDispatcher</a>
 

 

