---
UID: NF:winsvc.StartServiceCtrlDispatcherW
title: StartServiceCtrlDispatcherW function
author: windows-sdk-content
description: Connects the main thread of a service process to the service control manager, which causes the thread to be the service control dispatcher thread for the calling process.
old-location: base\startservicectrldispatcher.htm
tech.root: services
ms.assetid: 8e275eb7-a8af-4bd7-bb39-0eac4f3735ad
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: StartServiceCtrlDispatcher, StartServiceCtrlDispatcher function, StartServiceCtrlDispatcherA, StartServiceCtrlDispatcherW, _win32_startservicectrldispatcher, base.startservicectrldispatcher, winsvc/StartServiceCtrlDispatcher, winsvc/StartServiceCtrlDispatcherA, winsvc/StartServiceCtrlDispatcherW
ms.topic: function
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
 - API-MS-Win-Service-Winsvc-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-2-0.dll
 - API-Ms-Win-Service-Core-L1-1-2.dll
api_name:
 - StartServiceCtrlDispatcher
 - StartServiceCtrlDispatcherA
 - StartServiceCtrlDispatcherW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StartServiceCtrlDispatcherW function


## -description


Connects the main thread of a service process to the service control manager, which causes the thread to be the service control dispatcher thread for the calling process.


## -parameters




### -param lpServiceStartTable [in]

A pointer to an array of 
<a href="https://msdn.microsoft.com/dd40c4f0-cbbe-429f-91c0-3ba141dab702">SERVICE_TABLE_ENTRY</a> structures containing one entry for each service that can execute in the calling process. The members of the last entry in the table must have NULL values to designate the end of the table.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

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
<a href="https://msdn.microsoft.com/8e275eb7-a8af-4bd7-bb39-0eac4f3735ad">StartServiceCtrlDispatcher</a>. Each process can call 
<b>StartServiceCtrlDispatcher</b> only one time.

</td>
</tr>
</table>
 




## -remarks



When the service control manager starts a service process, it waits for the process to call the 
<b>StartServiceCtrlDispatcher</b> function. The main thread of a service process should make this call as soon as possible after it starts up (within 30 seconds). If 
<b>StartServiceCtrlDispatcher</b> succeeds, it connects the calling thread to the service control manager and does not return until all running services in the process have entered the SERVICE_STOPPED state. The service control manager uses this connection to send control and service start requests to the main thread of the service process. The main thread acts as a dispatcher by invoking the appropriate 
<a href="https://msdn.microsoft.com/bb1b863f-e29f-496f-a50e-9ea524fe8603">HandlerEx</a> function to handle control requests, or by creating a new thread to execute the appropriate 
<a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a> function when a new service is started.

The <i>lpServiceTable</i> parameter contains an entry for each service that can run in the calling process. Each entry specifies the 
<a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a> function for that service. For SERVICE_WIN32_SHARE_PROCESS services, each entry must contain the name of a service. This name is the service name that was specified by the 
<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> function when the service was installed. For SERVICE_WIN32_OWN_PROCESS services, the service name in the table entry is ignored.

If a service runs in its own process, the main thread of the service process should immediately call 
<b>StartServiceCtrlDispatcher</b>. All initialization tasks are done in the service's 
<a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a> function when the service is started.

If multiple services share a process and some common process-wide initialization needs to be done before any 
<a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a> function is called, the main thread can do the work before calling 
<b>StartServiceCtrlDispatcher</b>, as long as it takes less than 30 seconds. Otherwise, another thread must be created to do the process-wide initialization, while the main thread calls 
<b>StartServiceCtrlDispatcher</b> and becomes the service control dispatcher. Any service-specific initialization should still be done in the individual service main functions.

Services should not attempt to display a user interface directly. For more information, see <a href="https://msdn.microsoft.com/3d6e090a-00b1-47d8-a4fb-620f3db8ba9c">Interactive Services</a>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/7fdfc20a-9148-4ae1-8101-7a387c0d0edc">Writing a Service Program's Main Function</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/c112b587-7455-4f15-93e1-ded73de6dbbd">ControlService</a>



<a href="https://msdn.microsoft.com/bb1b863f-e29f-496f-a50e-9ea524fe8603">HandlerEx</a>



<a href="https://msdn.microsoft.com/dd40c4f0-cbbe-429f-91c0-3ba141dab702">SERVICE_TABLE_ENTRY</a>



<a href="https://msdn.microsoft.com/ed6945fc-ac08-4776-8d75-d33e8df3882a">Service Entry Point</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>



<a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a>
 

 

