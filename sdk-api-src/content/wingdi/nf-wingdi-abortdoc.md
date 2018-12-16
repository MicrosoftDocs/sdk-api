---
UID: NF:wingdi.AbortDoc
title: AbortDoc function
author: windows-sdk-content
description: The AbortDoc function stops the current print job and erases everything drawn since the last call to the StartDoc function.
old-location: gdi\abortdoc.htm
tech.root: printdocs
ms.assetid: 4ecc371c-34fa-4073-96fe-0de03b84d7e3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AbortDoc, AbortDoc function [Windows GDI], _win32_AbortDoc, gdi.abortdoc, wingdi/AbortDoc
ms.topic: function
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - API-MS-Win-GDI-Internal-Uap-L1-1-0.dll
api_name:
 - AbortDoc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AbortDoc function


## -description


The <b>AbortDoc</b> function stops the current print job and erases everything drawn since the last call to the <a href="https://msdn.microsoft.com/53143463-b9fc-4378-aea9-da6c73a7cd03">StartDoc</a> function.


## -parameters




### -param hdc [in]

Handle to the device context for the print job.


## -returns



If the function succeeds, the return value is greater than zero.

If the function fails, the return value is SP_ERROR.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
Applications should call the <b>AbortDoc</b> function to stop a print job if an error occurs, or to stop a print job after the user cancels that job. To end a successful print job, an application should call the <a href="https://msdn.microsoft.com/bf63ea0f-cc73-4943-9c84-52b3b77e141c">EndDoc</a> function.

If Print Manager was used to start the print job, calling <b>AbortDoc</b> erases the entire spool job, so that the printer receives nothing. If Print Manager was not used to start the print job, the data may already have been sent to the printer. In this case, the printer driver resets the printer (when possible) and ends the print job.




## -see-also




<a href="https://msdn.microsoft.com/bf63ea0f-cc73-4943-9c84-52b3b77e141c">EndDoc</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/e5c115b0-9c1e-46e7-8fb5-eddbc2c75298">Printing</a>



<a href="https://msdn.microsoft.com/5b6333fc-f1c3-4c76-906c-0fd13bb73953">SetAbortProc</a>



<a href="https://msdn.microsoft.com/53143463-b9fc-4378-aea9-da6c73a7cd03">StartDoc</a>
 

 

