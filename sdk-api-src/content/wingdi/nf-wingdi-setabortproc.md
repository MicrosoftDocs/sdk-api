---
UID: NF:wingdi.SetAbortProc
title: SetAbortProc function
author: windows-sdk-content
description: The SetAbortProc function sets the application-defined abort function that allows a print job to be canceled during spooling.
old-location: gdi\setabortproc.htm
tech.root: printdocs
ms.assetid: 5b6333fc-f1c3-4c76-906c-0fd13bb73953
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: SetAbortProc, SetAbortProc function [Windows GDI], _win32_SetAbortProc, gdi.setabortproc, wingdi/SetAbortProc
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - SetAbortProc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetAbortProc function


## -description


The <b>SetAbortProc</b> function sets the application-defined abort function that allows a print job to be canceled during spooling.


## -parameters




### -param hdc [in]

Handle to the device context for the print job.


### -param proc [in]

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



<a href="https://msdn.microsoft.com/e5c115b0-9c1e-46e7-8fb5-eddbc2c75298">Printing</a>
 

 

