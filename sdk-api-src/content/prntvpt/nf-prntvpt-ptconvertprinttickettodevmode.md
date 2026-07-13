---
UID: NF:prntvpt.PTConvertPrintTicketToDevMode
title: PTConvertPrintTicketToDevMode function (prntvpt.h)
description: Converts a print ticket into a DEVMODE structure.
helpviewer_keywords: ["PTConvertPrintTicketToDevMode","PTConvertPrintTicketToDevMode function [Windows GDI]","_win32_PTConvertPrintTicketToDevMode","gdi.ptconvertprinttickettodevmode","prntvpt/PTConvertPrintTicketToDevMode"]
old-location: gdi\ptconvertprinttickettodevmode.htm
tech.root: xps
ms.assetid: 5eec91b9-d554-4440-bc9e-6a26af34994b
ms.date: 12/05/2018
ms.keywords: PTConvertPrintTicketToDevMode, PTConvertPrintTicketToDevMode function [Windows GDI], _win32_PTConvertPrintTicketToDevMode, gdi.ptconvertprinttickettodevmode, prntvpt/PTConvertPrintTicketToDevMode
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
 - PTConvertPrintTicketToDevMode
 - prntvpt/PTConvertPrintTicketToDevMode
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
api_name:
 - PTConvertPrintTicketToDevMode
---

# PTConvertPrintTicketToDevMode function


## -description

Converts a print ticket into a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure.

## -parameters

### -param hProvider [in]

A handle to an opened print ticket provider. This handle is returned by the <a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider">PTOpenProvider</a> or the <a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex">PTOpenProviderEx</a> function.

### -param pPrintTicket [in]

A pointer to an <a href="/windows/desktop/Stg/istream-compound-file-implementation">IStream</a> with its seek position at the beginning of the print ticket.

### -param baseDevmodeType

A value indicating whether the user's default <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> or the print queue's default <b>DEVMODE</b> is used to provide values to the output <b>DEVMODE</b> when <i>pPrintTicket</i> does not specify every possible setting for a <b>DEVMODE</b>.

### -param scope [in]

A value that specifies the scope of <i>pPrintTicket</i>. This value can specify a single page, an entire document, or all documents in the print job. Settings in <i>pPrintTicket</i> that are outside of the specified scope are ignored. See Remarks.

### -param pcbDevmode [out]

A pointer to the size of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> in bytes.

### -param ppDevmode [out]

A pointer to the newly created <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a>.

### -param pbstrErrorMessage [out]

A pointer to a string that specifies what, if anything, is invalid about <i>pPrintTicket</i>. If it is valid, this is <b>NULL</b>.

## -returns

If the operation succeeds, the return value is S_OK.

If <i>hProvider</i> was opened in a different thread, the <b>HRESULT</b> is E_INVALIDARG.

If <i>pPrintTicket</i> is invalid, the <b>HRESULT</b> is E_PRINTTICKET_FORMAT.

Otherwise, some other error code is returned in the <b>HRESULT</b>. For more information about COM error codes, see <a href="/windows/desktop/SetupApi/error-handling">Error Handling</a>.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The <i>hProvider</i> parameter must be a handle that was opened in the same thread as the thread in which it is used for this function. 
      

If <i>baseDevmodeType</i> is kUserDefaultDevmode, but the user's default is not available, then the device's default will be used.

The returned <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> may be internally inconsistent or conflict with hard printer settings even though each setting within it is viable individually. For example, if the printer supports an optional duplexer but the <i>pPrintTicket</i> calls for duplexing, then the returned <b>DEVMODE</b> will also call for duplexing, even if the duplexer is not installed. Use <a href="/windows/desktop/printdocs/documentproperties">DocumentProperties</a> to correct the returned <b>DEVMODE</b>.

The buffer in the returned <i>ppDevmode</i> should be released with <a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptreleasememory">PTReleaseMemory</a>.

Values of <i>pPrintTicket</i> that are outside of the <i>scope</i> are ignored. For example, if the scope is only a single page, then job-wide settings and document-wide settings are ignored. Job scope includes document scope and page scope. Document scope includes page scope.

If <i>pbstrErrorMessage</i> is not <b>NULL</b> when the function returns, the caller must free the string with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

## -see-also

<a href="/windows/desktop/printdocs/printschema">Print Schema</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>