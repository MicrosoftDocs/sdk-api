---
UID: NF:prntvpt.PTConvertDevModeToPrintTicket
title: PTConvertDevModeToPrintTicket function (prntvpt.h)

description: Converts a DEVMODE structure to a print ticket inside an IStream.
old-location: gdi\ptconvertdevmodetoprintticket.htm
tech.root: printdocs
ms.assetid: 22ebb9e7-10c6-4512-b749-d61f74bc82ed

ms.date: 12/05/2018
ms.keywords: PTConvertDevModeToPrintTicket, PTConvertDevModeToPrintTicket function [Windows GDI], _win32_PTConvertDevModeToPrintTicket, gdi.ptconvertdevmodetoprintticket, prntvpt/PTConvertDevModeToPrintTicket
ms.topic: function
f1_keywords: 
 - "prntvpt/PTConvertDevModeToPrintTicket"
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
 - Ext-MS-Win-printer-prntvpt-l1-1-0.dll
api_name:
 - PTConvertDevModeToPrintTicket
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PTConvertDevModeToPrintTicket function


## -description


Converts a <a href="https://docs.microsoft.com/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure to a print ticket inside an <a href="https://docs.microsoft.com/windows/desktop/Stg/istream-compound-file-implementation">IStream</a>.


## -parameters




### -param hProvider [in]

A handle to an open print ticket provider. This handle is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider">PTOpenProvider</a> or the <a href="https://docs.microsoft.com/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex">PTOpenProviderEx</a> function.


### -param cbDevmode

The size of the <a href="https://docs.microsoft.com/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> in bytes.


### -param pDevmode [in]

A pointer to the <a href="https://docs.microsoft.com/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a>.


### -param scope [in]

A value that specifies the scope of <i>pPrintTicket</i>. This value can specify a single page, an entire document, or all documents in the print job. Settings in <i>pDevmode</i> that are outside the specified scope will not be included in <i>pPrintTicket</i>. See Remarks.


### -param pPrintTicket

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/Stg/istream-compound-file-implementation">IStream</a> with its seek position at the beginning of the print ticket.


## -returns



If the operation succeeds, the return value is S_OK, otherwise the <b>HRESULT</b> contains an error code.

If <i>hProvider</i> was opened in a different thread, the <b>HRESULT</b> is E_INVALIDARG.

For more information about COM error codes, see <a href="https://docs.microsoft.com/windows/desktop/SetupApi/error-handling">Error Handling</a>.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
<i>hProvider</i> must be a handle that was opened in the same thread as the thread in which it is used for this function.
      

If the <i>pDevmode</i> points to a different printer, its settings may be lost and replaced with defaults.

Settings in <i>pDevmode</i> that are outside the <i>scope</i> are not included in <i>pPrintTicket</i>. For example, if the scope is a single page, then job-wide settings and document-wide settings are not included. A job scope includes document scope and page scope. A document scope includes page scope.

<b>PTConvertDevModeToPrintTicket</b> writes the print ticket to the <a href="https://docs.microsoft.com/windows/desktop/Stg/istream-compound-file-implementation">IStream</a> referenced by <i>pPrintTicket</i> starting at the stream's current seek point. After <b>PTConvertDevModeToPrintTicket</b> returns, the caller must reset the seek point to the initial seek point to read the print ticket returned by the function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/printdocs/printschema">Print Schema</a>



<a href="https://docs.microsoft.com/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/printdocs/printdocs-printing">Printing</a>
 

 

