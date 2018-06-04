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

# RoFailFastWithErrorContext function


## -description


Raises a non-continuable exception in the current process.


## -parameters




### -param hrError [in]

The <b>HRESULT</b> associated with the current error. The exception is raised for any value of <i>hrError</i>.


## -returns



This function does not return a value.




## -remarks



The <b>RoFailFastWithErrorContext</b> function raises a non-continuable exception in the current process when an unhandled failure is encountered, which  prevents the process from continuing execution in an undefined state.

Call the <b>RoFailFastWithErrorContext</b> function when a failure occurs in a completion delegate for a completed asynchronous operation, or  when a failure occurs in an event handler when an event is raised.

The process that calls <b>RoFailFastWithErrorContext</b> is terminated by a call to <a href="https://msdn.microsoft.com/69fbb722-2733-4035-8bfa-a5828311581c">RaiseFailFastException</a>.  The function does not validate the parameters and raises an exception for any value of the inputs.

Call the <a href="https://msdn.microsoft.com/4102CAD6-B5EC-4633-91CC-D56F6C0E287E">RoCaptureErrorContext</a> function to save an <a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a> object that's associated with the current thread. The <b>RoFailFastWithErrorContext</b> function uses this contextual information to report the error call stack to the Windows Error Reporting service (WER), if it's enabled.




## -see-also




<a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a>



<a href="https://msdn.microsoft.com/69fbb722-2733-4035-8bfa-a5828311581c">RaiseFailFastException</a>



<a href="https://msdn.microsoft.com/4102CAD6-B5EC-4633-91CC-D56F6C0E287E">RoCaptureErrorContext</a>
 

 

