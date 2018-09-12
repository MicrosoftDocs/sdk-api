---
UID: NF:prntvpt.PTCloseProvider
title: PTCloseProvider function
author: windows-sdk-content
description: Closes a print ticket provider handle.
old-location: gdi\ptcloseprovider.htm
tech.root: printdocs
ms.assetid: 28e85b53-fd0c-4210-ae2b-794efaf65bd4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PTCloseProvider, PTCloseProvider function [Windows GDI], _win32_PTCloseProvider, gdi.ptcloseprovider, prntvpt/PTCloseProvider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: prntvpt.h
req.include-header: 
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
req.lib: Prntvpt.lib
req.dll: Prntvpt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - prntvpt.dll
 - Ext-MS-Win-printer-prntvpt-l1-1-0.dll
api_name:
 - PTCloseProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PTCloseProvider function


## -description


Closes a print ticket provider handle.


## -parameters




### -param hProvider [in]

A handle to the provider. This handle is returned by the <a href="https://msdn.microsoft.com/6821b1b0-74b0-4caf-b8e6-a9df4d7693d7">PTOpenProvider</a> or <a href="https://msdn.microsoft.com/0e65170b-66f6-4238-bdde-0a0b7108a686">PTOpenProviderEx</a> function.


## -returns



If the operation succeeds, the return value is S_OK, otherwise the <b>HRESULT</b> contains an error code.

If <i>hProvider</i> was opened in a different thread, the <b>HRESULT</b> is E_INVALIDARG.

For more information about COM error codes, see <a href="_com_error_handling">Error Handling</a>.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The <i>hProvider</i> parameter must be a handle that was opened in the same thread as the thread in which it is used for this function. 
      

A handle cannot be used after it is closed.




## -see-also




<a href="https://msdn.microsoft.com/98d5f8ec-54bd-4e88-b632-ed427b599cb6">Print Schema</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/e5c115b0-9c1e-46e7-8fb5-eddbc2c75298">Printing</a>
 

 

