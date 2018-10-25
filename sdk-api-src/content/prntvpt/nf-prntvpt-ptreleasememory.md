---
UID: NF:prntvpt.PTReleaseMemory
title: PTReleaseMemory function
author: windows-sdk-content
description: Releases buffers associated with print tickets and print capabilities.
old-location: gdi\ptreleasememory.htm
tech.root: printdocs
ms.assetid: d568b3a9-7f13-4e4e-8bbc-f4ab0009fe83
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: PTReleaseMemory, PTReleaseMemory function [Windows GDI], _win32_PTReleaseMemory, gdi.ptreleasememory, prntvpt/PTReleaseMemory
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
api_name:
 - PTReleaseMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PTReleaseMemory function


## -description


Releases buffers associated with print tickets and print capabilities.


## -parameters




### -param pBuffer [in]

A pointer to a buffer allocated during a call to a print ticket API.


## -returns



If the operation succeeds, the return value is S_OK, otherwise the <b>HRESULT</b> contains an error code.

For more information about COM error codes, see <a href="_com_error_handling">Error Handling</a>.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
Use this function to release the <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> buffer returned by <a href="https://msdn.microsoft.com/5eec91b9-d554-4440-bc9e-6a26af34994b">PTConvertPrintTicketToDevMode</a>.




## -see-also




<a href="https://msdn.microsoft.com/98d5f8ec-54bd-4e88-b632-ed427b599cb6">Print Schema</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/e5c115b0-9c1e-46e7-8fb5-eddbc2c75298">Printing</a>
 

 

