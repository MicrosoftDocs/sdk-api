---
UID: NF:prntvpt.PTMergeAndValidatePrintTicket
title: PTMergeAndValidatePrintTicket function (prntvpt.h)
description: Merges two print tickets and returns a valid, viable print ticket.
helpviewer_keywords: ["PTMergeAndValidatePrintTicket","PTMergeAndValidatePrintTicket function [Windows GDI]","_win32_PTMergeAndValidatePrintTicket","gdi.ptmergeandvalidateprintticket","prntvpt/PTMergeAndValidatePrintTicket"]
old-location: gdi\ptmergeandvalidateprintticket.htm
tech.root: xps
ms.assetid: 97691930-d76a-48c9-80b9-8413d96322a9
ms.date: 12/05/2018
ms.keywords: PTMergeAndValidatePrintTicket, PTMergeAndValidatePrintTicket function [Windows GDI], _win32_PTMergeAndValidatePrintTicket, gdi.ptmergeandvalidateprintticket, prntvpt/PTMergeAndValidatePrintTicket
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
 - PTMergeAndValidatePrintTicket
 - prntvpt/PTMergeAndValidatePrintTicket
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-printer-prntvpt-l1-1-2.dll
 - prntvpt.dll
api_name:
 - PTMergeAndValidatePrintTicket
---

# PTMergeAndValidatePrintTicket function


## -description

Merges two print tickets and returns a valid, viable print ticket.

## -parameters

### -param hProvider [in]

A handle to an open print ticket provider. This handle is returned by the <a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider">PTOpenProvider</a> or the <a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex">PTOpenProviderEx</a> function.

### -param pBaseTicket [in]

A pointer to a print ticket. The stream's seek position must be at the beginning of the print ticket content. 

<div class="alert"><b>Note</b>  <b>PTMergeAndValidatePrintTicket</b> will validate the base ticket against the <a href="/windows/desktop/printdocs/printschema">Print Schema Framework</a> before merging.</div>
<div> </div>

### -param pDeltaTicket [in]

A pointer to a print ticket. The stream's seek position must be at the beginning of the print ticket content. <b>NULL</b> can be passed to this parameter. See Remarks. 

<div class="alert"><b>Note</b>  <b>PTMergeAndValidatePrintTicket</b> will validate the delta ticket against the <a href="/windows/desktop/printdocs/printschema">Print Schema Framework</a> before merging.</div>
<div> </div>

### -param scope [in]

A value specifying whether the scope of <i>pDeltaTicket</i> and <i>pResultTicket</i> is a single page, an entire document, or all documents in the print job. See Remarks.

### -param pResultTicket

A pointer to the stream where the viable, merged ticket will be written. The seek position will be at the end of the print ticket. See Remarks.

### -param pbstrErrorMessage [out]

A pointer to a string that specifies what, if anything, is invalid about <i>pBaseTicket</i> or <i>pDeltaTicket</i>. If both are valid, this is <b>NULL</b>. Viability problems are not reported in <i>pbstrErrorMessage</i>.

## -returns

If the operation succeeds with no conflict between the settings of the merged ticket and the capabilities of the printer, the <b>HRESULT</b> is S_PT_NO_CONFLICT.

If the operation succeeds but the merged ticket had to be changed in one or more settings because it requested functionality that the printer does not support, the <b>HRESULT</b> is S_PT_CONFLICT_RESOLVED. See Remarks.

If <i>hProvider</i> was opened in a different thread, the <b>HRESULT</b> is E_INVALIDARG.

If <i>pBaseTicket</i> is invalid, the <b>HRESULT</b> is E_PRINTTICKET_FORMAT.

If <i>pDeltaTicket</i> is invalid, the <b>HRESULT</b> is E_DELTA_PRINTTICKET_FORMAT.

Otherwise, some other error code is returned in the <b>HRESULT</b>. For more information about COM error codes, see <a href="/windows/desktop/SetupApi/error-handling">Error Handling</a>.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
<i>hProvider</i> must be a handle that was opened in the same thread as the thread in which it is used for this function. 
      

This function validates in two ways: It first validates both input tickets against the <a href="/windows/desktop/printdocs/printschema">Print Schema Framework</a>, reporting errors in <i>pbstrErrorMessage</i>. It then checks the viability of the merged print ticket with the printer driver. If the merged ticket requests functionality that the printer does not support, the nonviable settings are replaced and the printer driver determines what substitute setting to use. Typically, the printer driver uses the user's default print ticket setting. If the printer driver does not use the same print ticket that <i>pBaseTicket</i> points to as the source for substitute values, it is possible that <i>pResultTicket</i> will differ in some settings from both of the input print tickets.

Typically, <i>pBaseTicket</i> contains a full range of job, document and page settings. Usually the user default or the device default print ticket is used for <i>pBaseTicket</i>.

If <i>pDeltaTicket</i> is <b>NULL</b>, the method validates <i>pBaseTicket</i>, checks its viability, and returns it, possibly modified, in the stream pointed to by <i>pResultTicket</i>.

Values of <i>pDeltaTicket</i> that are outside of the <i>scope</i> are ignored. For example, if the scope is only a single page, then job-wide settings and document-wide settings are ignored. Job scope includes document scope and page scope. Document scope includes page scope.

Settings that are outside of the <i>scope</i> are not included in the <i>pResultTicket</i>.

When the function returns a value, the seek position of <i>pResultTicket</i> is at the end of the print ticket content. The caller is responsible for resetting the seek position before reading the data.

If <i>pbstrErrorMessage</i> is not <b>NULL</b> when the function returns, the caller must free the string with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

## -see-also

<a href="/windows/desktop/printdocs/printschema">Print Schema</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>