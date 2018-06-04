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

# SetAbortProc function


## -description


The <b>SetAbortProc</b> function sets the application-defined abort function that allows a print job to be canceled during spooling.


## -parameters




### -param hdc [in]

Handle to the device context for the print job.


### -param proc

TBD




#### - lpAbortProc [in]

Pointer to the application-defined abort function. For more information about the callback function, see the <a href="https://msdn.microsoft.com/3728a491-28ff-49ec-9131-ed6238b2be3d">AbortProc</a> callback function.


## -returns



If the function succeeds, the return value is greater than zero.

If the function fails, the return value is SP_ERROR.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>

#### Examples

For an example, see <a href="https://msdn.microsoft.com/98ae97e2-25c1-455c-8283-45bb07fb8251">How to Collect Print Job  Information from the User</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4ecc371c-34fa-4073-96fe-0de03b84d7e3">AbortDoc</a>



<a href="https://msdn.microsoft.com/3728a491-28ff-49ec-9131-ed6238b2be3d">AbortProc</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

