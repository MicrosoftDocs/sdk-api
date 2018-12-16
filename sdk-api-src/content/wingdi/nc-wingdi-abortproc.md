---
UID: NC:wingdi.ABORTPROC
title: ABORTPROC
author: windows-sdk-content
description: The AbortProc function is an application-defined callback function used with the SetAbortProc function.
old-location: gdi\abortproc.htm
tech.root: printdocs
ms.assetid: 3728a491-28ff-49ec-9131-ed6238b2be3d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AbortProc, AbortProc callback, AbortProc callback function [Windows GDI], _win32_AbortProc, gdi.abortproc, wingdi/AbortProc
ms.topic: callback
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Wingdi.h
api_name:
 - AbortProc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
If the <i>iError</i> parameter is SP_OUTOFDISK, the application need not cancel the print job. If it does not cancel the job, it must yield to Print Manager by calling the <a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a> or <a href="https://msdn.microsoft.com/en-us/library/Aa359047(v=VS.85).aspx">GetMessage</a> function.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa359047(v=VS.85).aspx">GetMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/e5c115b0-9c1e-46e7-8fb5-eddbc2c75298">Printing</a>



<a href="https://msdn.microsoft.com/5b6333fc-f1c3-4c76-906c-0fd13bb73953">SetAbortProc</a>
 

 

