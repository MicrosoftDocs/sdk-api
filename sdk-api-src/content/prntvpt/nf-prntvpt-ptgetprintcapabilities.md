---
UID: NF:prntvpt.PTGetPrintCapabilities
title: PTGetPrintCapabilities function (prntvpt.h)
description: Retrieves the printer's capabilities formatted in compliance with the XML Print Schema.
helpviewer_keywords: ["PTGetPrintCapabilities","PTGetPrintCapabilities function [Windows GDI]","_win32_PTGetPrintCapabilities","gdi.ptgetprintcapabilities","prntvpt/PTGetPrintCapabilities"]
old-location: gdi\ptgetprintcapabilities.htm
tech.root: xps
ms.assetid: 925e314c-85ff-4c1b-b3c9-f36aa4b55e01
ms.date: 12/05/2018
ms.keywords: PTGetPrintCapabilities, PTGetPrintCapabilities function [Windows GDI], _win32_PTGetPrintCapabilities, gdi.ptgetprintcapabilities, prntvpt/PTGetPrintCapabilities
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
 - PTGetPrintCapabilities
 - prntvpt/PTGetPrintCapabilities
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
 - PTGetPrintCapabilities
---

# PTGetPrintCapabilities function


## -description

Retrieves the printer's capabilities formatted in compliance with the XML <a href="/windows/desktop/printdocs/printschema">Print Schema</a>.

## -parameters

### -param hProvider [in]

A handle to an open provider whose print capabilities are to be retrieved. This handle is returned by the <a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider">PTOpenProvider</a> or the <a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex">PTOpenProviderEx</a> function.

### -param pPrintTicket [in]

A pointer to a stream with its seek position at the beginning of the print ticket content. This parameter can be <b>NULL</b>.

### -param pCapabilities

A pointer to the stream where the print capabilities will be written, starting at the current seek position.

### -param pbstrErrorMessage [out]

A pointer to a string that specifies what, if anything, is invalid about <i>pPrintTicket</i>. If it is valid, this value is <b>NULL</b>.

## -returns

If the operation succeeds, the return value is S_OK.

If <i>hProvider</i> was opened in a different thread, the <b>HRESULT</b> is E_INVALIDARG.

If the <i>pPrintTicket</i> is not compliant with the <a href="/windows/desktop/printdocs/printschema">Print Schema</a> , the <b>HRESULT</b> is E_PRINTTICKET_FORMAT.

If the <i>pCapabilities</i> is not compliant with the <a href="/windows/desktop/printdocs/printschema">Print Schema</a> , the <b>HRESULT</b> is E_PRINTCAPABILITIES_FORMAT.

If <i>hProvider</i> was opened in a different thread, the <b>HRESULT</b> is E_INVALIDARG.

Otherwise, another error code is returned in the <b>HRESULT</b>. For more information about COM error codes, see <a href="/windows/desktop/SetupApi/error-handling">Error Handling</a>.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
<i>hProvider</i> must be a handle that was opened in the same thread as the thread in which it is used for this function. 
      

The printer driver uses <i>pPrintTicket</i> values (when the value is not <b>NULL</b>) to create settings when the driver produces printer capabilities that vary depending on the current settings.

When the function returns, the seek position of <i>pPrintTicket</i> is at the end of the print ticket content and the seek position of <i>pCapabilities</i> is at the end of the stream. If the caller uses a memory stream for <i>pCapabilities</i>, such as a stream created by <a href="/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal">CreateStreamOnHGlobal</a> , the caller is responsible for resetting the seek position before reading the data.

If <i>pbstrErrorMessage</i> is not <b>NULL</b> when the function returns, the caller must free the string with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

## -see-also

<a href="/windows/desktop/printdocs/printschema">Print Schema</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>