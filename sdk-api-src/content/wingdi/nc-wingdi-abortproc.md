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

# ABORTPROC callback function


## -description


The <b>AbortProc</b> function is an application-defined callback function used with the <a href="https://msdn.microsoft.com/5b6333fc-f1c3-4c76-906c-0fd13bb73953">SetAbortProc</a> function. It is called when a print job is to be canceled during spooling. The <b>ABORTPROC</b> type defines a pointer to this callback function. <b>AbortProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param Arg1


### -param Arg2








#### - hdc [in]

A handle to the device context for the print job.


#### - iError [in]

Specifies whether an error has occurred. This parameter is zero if no error has occurred; it is SP_OUTOFDISK if Print Manager is currently out of disk space and more disk space will become available if the application waits.


## -returns



The callback function should return <b>TRUE</b> to continue the print job or <b>FALSE</b> to cancel the print job.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
If the <i>iError</i> parameter is SP_OUTOFDISK, the application need not cancel the print job. If it does not cancel the job, it must yield to Print Manager by calling the <a href="_win32_peekmessage_cpp">PeekMessage</a> or <a href="_win32_getmessage_cpp">GetMessage</a> function.




## -see-also




<a href="_win32_getmessage_cpp">GetMessage</a>



<a href="_win32_peekmessage_cpp">PeekMessage</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/5b6333fc-f1c3-4c76-906c-0fd13bb73953">SetAbortProc</a>
 

 

