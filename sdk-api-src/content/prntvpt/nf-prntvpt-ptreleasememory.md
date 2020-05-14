---
UID: NF:prntvpt.PTReleaseMemory
title: PTReleaseMemory function (prntvpt.h)
description: Releases buffers associated with print tickets and print capabilities.
helpviewer_keywords: ["PTReleaseMemory","PTReleaseMemory function [Windows GDI]","_win32_PTReleaseMemory","gdi.ptreleasememory","prntvpt/PTReleaseMemory"]
old-location: gdi\ptreleasememory.htm
tech.root: printdocs
ms.assetid: d568b3a9-7f13-4e4e-8bbc-f4ab0009fe83
ms.date: 12/05/2018
ms.keywords: PTReleaseMemory, PTReleaseMemory function [Windows GDI], _win32_PTReleaseMemory, gdi.ptreleasememory, prntvpt/PTReleaseMemory
f1_keywords:
- prntvpt/PTReleaseMemory
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PTReleaseMemory function


## -description


Releases buffers associated with print tickets and print capabilities.


## -parameters




### -param pBuffer [in]

A pointer to a buffer allocated during a call to a print ticket API.


## -returns



If the operation succeeds, the return value is S_OK, otherwise the <b>HRESULT</b> contains an error code.

For more information about COM error codes, see <a href="https://docs.microsoft.com/windows/desktop/SetupApi/error-handling">Error Handling</a>.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
Use this function to release the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> buffer returned by <a href="https://docs.microsoft.com/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode">PTConvertPrintTicketToDevMode</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/printdocs/printschema">Print Schema</a>



<a href="https://docs.microsoft.com/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/printdocs/printdocs-printing">Printing</a>
 

 

