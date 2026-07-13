---
UID: NF:prntvpt.PTCloseProvider
title: PTCloseProvider function (prntvpt.h)
description: Closes a print ticket provider handle.
helpviewer_keywords: ["PTCloseProvider","PTCloseProvider function [Windows GDI]","_win32_PTCloseProvider","gdi.ptcloseprovider","prntvpt/PTCloseProvider"]
old-location: gdi\ptcloseprovider.htm
tech.root: xps
ms.assetid: 28e85b53-fd0c-4210-ae2b-794efaf65bd4
ms.date: 12/05/2018
ms.keywords: PTCloseProvider, PTCloseProvider function [Windows GDI], _win32_PTCloseProvider, gdi.ptcloseprovider, prntvpt/PTCloseProvider
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PTCloseProvider
 - prntvpt/PTCloseProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-printer-prntvpt-l1-1-2.dll
 - ext-ms-win-printer-prntvpt-l1-1-1.dll
 - prntvpt.dll
 - Ext-MS-Win-printer-prntvpt-l1-1-0.dll
api_name:
 - PTCloseProvider
---

# PTCloseProvider function


## -description

Closes a print ticket provider handle.

## -parameters

### -param hProvider [in]

A handle to the provider. This handle is returned by the <a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider">PTOpenProvider</a> or <a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex">PTOpenProviderEx</a> function.

## -returns

If the operation succeeds, the return value is S_OK, otherwise the <b>HRESULT</b> contains an error code.

If <i>hProvider</i> was opened in a different thread, the <b>HRESULT</b> is E_INVALIDARG.

For more information about COM error codes, see <a href="/windows/desktop/SetupApi/error-handling">Error Handling</a>.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The <i>hProvider</i> parameter must be a handle that was opened in the same thread as the thread in which it is used for this function. 
      

A handle cannot be used after it is closed.

## -see-also

<a href="/windows/desktop/printdocs/printschema">Print Schema</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>