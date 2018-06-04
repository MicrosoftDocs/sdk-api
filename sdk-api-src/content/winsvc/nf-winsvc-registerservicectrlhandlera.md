---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# RegisterServiceCtrlHandlerA function


## -description


Registers a function to handle  service control requests.

This function has been superseded by the 
<a href="https://msdn.microsoft.com/23eea346-9899-4214-88f4-9b7eb7ce1332">RegisterServiceCtrlHandlerEx</a> function. A service can use either function, but the new function supports user-defined context data, and the new handler function supports additional extended control codes.


## -parameters




### -param lpServiceName [in]

The name of the service run by the calling thread. This is the service name that the service control program specified in the 
<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> function when creating the service. 




If the service type is SERVICE_WIN32_OWN_PROCESS, the function does not verify that the specified name is valid, because there is only one registered service in the process.


### -param lpHandlerProc [in]

A pointer to the handler function to be registered. For more information, see 
<a href="https://msdn.microsoft.com/e2d6d3a7-070e-4343-abd7-b4b9f8dd6fbc">Handler</a>.


## -returns



If the function succeeds, the return value is a service status handle.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following error codes can be set by the service control manager. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available to convert an ANSI string parameter to Unicode. This error does not occur for Unicode string parameters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_NOT_IN_EXE</b></dt>
</dl>
</td>
<td width="60%">
The service entry was specified incorrectly when the process called the <a href="https://msdn.microsoft.com/8e275eb7-a8af-4bd7-bb39-0eac4f3735ad">StartServiceCtrlDispatcher</a> function.

</td>
</tr>
</table>
 




## -remarks



The 
<a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a> function of a new service should immediately call the 
<b>RegisterServiceCtrlHandler</b> function to register a control handler function with the control dispatcher. This enables the control dispatcher to invoke the specified function when it receives control requests for this service. For a list of possible control codes, see <a href="https://msdn.microsoft.com/e2d6d3a7-070e-4343-abd7-b4b9f8dd6fbc">Handler</a>. The threads of the calling process can use the service status handle returned by this function to identify the service in subsequent calls to the 
<a href="https://msdn.microsoft.com/bb5943ff-2814-40f2-bee0-ae7132befde9">SetServiceStatus</a> function.

The 
<b>RegisterServiceCtrlHandler</b> function must be called before the first 
<a href="https://msdn.microsoft.com/bb5943ff-2814-40f2-bee0-ae7132befde9">SetServiceStatus</a> call because 
<b>RegisterServiceCtrlHandler</b> returns a service status handle for the caller to use so that no other service can inadvertently set this service status. In addition, the control handler must be in place to receive control requests by the time the service specifies the controls it accepts through the 
<b>SetServiceStatus</b> function.

When the control handler function is invoked with a control request, the service must call 
<a href="https://msdn.microsoft.com/bb5943ff-2814-40f2-bee0-ae7132befde9">SetServiceStatus</a> to report status to the service control manager only if the service status has changed, such as when the service is processing stop or shutdown controls. If the service status has not changed, the service should not report status to the service control manager. 

The service status handle does not have to be closed.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/7aa9371d-676c-4633-9831-edf0e74d15f0">Writing a ServiceMain Function</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a>



<a href="https://msdn.microsoft.com/e2d6d3a7-070e-4343-abd7-b4b9f8dd6fbc">Handler</a>



<a href="https://msdn.microsoft.com/23eea346-9899-4214-88f4-9b7eb7ce1332">RegisterServiceCtrlHandlerEx</a>



<a href="https://msdn.microsoft.com/437334ed-05fa-4ab6-aab3-dc2739113e19">Service Control Handler Function</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>



<a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a>



<a href="https://msdn.microsoft.com/bb5943ff-2814-40f2-bee0-ae7132befde9">SetServiceStatus</a>
 

 

