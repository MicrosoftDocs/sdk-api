---
UID: NF:winfax.FaxStartPrintJobA
title: FaxStartPrintJobA function (winfax.h)
description: A fax client application calls the FaxStartPrintJob function to start printing an outbound fax transmission on the specified fax printer. (ANSI)
helpviewer_keywords: ["FaxStartPrintJobA", "winfax/FaxStartPrintJobA"]
old-location: fax\_mfax_faxstartprintjob.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3dwi.htm
ms.date: 12/05/2018
ms.keywords: FaxStartPrintJob, FaxStartPrintJob function [Fax Service], FaxStartPrintJobA, FaxStartPrintJobW, _mfax_faxstartprintjob, fax._mfax_faxstartprintjob, winfax/FaxStartPrintJob, winfax/FaxStartPrintJobA, winfax/FaxStartPrintJobW
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxStartPrintJobW (Unicode) and FaxStartPrintJobA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WinFax.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FaxStartPrintJobA
 - winfax/FaxStartPrintJobA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - WinFax.lib
 - WinFax.dll
api_name:
 - FaxStartPrintJob
 - FaxStartPrintJobA
 - FaxStartPrintJobW
---

# FaxStartPrintJobA function


## -description

A fax client application calls the <b>FaxStartPrintJob</b> function to start printing an outbound fax transmission on the specified fax printer.

## -parameters

### -param PrinterName [in]

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that contains the name of a fax printer. The string can specify one of the following: 

                    


<ul>
<li>A local printer, such as, "<i>printername</i>"</li>
<li>A network printer, such as "&#92;&#92;<i>machinename</i>&#92;<i>printername</i>"</li>
<li><b>NULL</b> to specify the local fax printer</li>
</ul>

### -param PrintInfo [in]

Type: <b>const <a href="/windows/desktop/api/winfax/ns-winfax-fax_print_infoa">FAX_PRINT_INFO</a>*</b>

Pointer to a <a href="/windows/desktop/api/winfax/ns-winfax-fax_print_infoa">FAX_PRINT_INFO</a> structure that contains the information necessary for the fax server to print the fax transmission. The structure includes, among other items, the recipient's fax number, sender and recipient data, an optional billing code, and delivery report information. For more information, see the following Remarks section.

### -param FaxJobId [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the print spooler's unique ID for the fax print job. (This is not the same as the fax queue's ID for the job and it cannot be used as a parameter in any fax API that takes a fax ID parameter.) This parameter is required.

### -param FaxContextInfo [out]

Type: <b>PFAX_CONTEXT_INFO</b>

Pointer to a <a href="/windows/desktop/api/winfax/ns-winfax-fax_context_infoa">FAX_CONTEXT_INFO</a> structure to receive a handle to a printer device context. When the fax client application calls the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxprintcoverpagea">FaxPrintCoverPage</a> function, it must pass this value in that function's <i>FaxContextInfo</i> parameter. For more information, see <a href="/windows/desktop/gdi/device-contexts">Device Contexts</a> and the <a href="/previous-versions/ms535790(v=vs.85)">Printing and Print Spooler Reference</a>.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. GetLastError can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or both of the <i>PrintInfo</i> or <i>FaxContextInfo</i> parameters are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <b>RecipientNumber</b> member of the <a href="/windows/desktop/api/winfax/ns-winfax-fax_print_infoa">FAX_PRINT_INFO</a> structure is <b>NULL</b>; or the <b>OutputFileName</b> member is <b>NULL</b> and the <b>RecipientNumber</b> member is not specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PRINTER_NAME</b></dt>
</dl>
</td>
<td width="60%">
The <i>PrinterName</i> parameter specifies a printer that is not a fax printer, or there is no fax printer installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during memory allocation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SPL_NO_STARTDOC</b></dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxstartprintjoba">FaxStartPrintJob</a> was not called first, hence there was no <a href="/windows/desktop/api/wingdi/nf-wingdi-startdoca">StartDoc</a> call.

</td>
</tr>
</table>

## -remarks

The function returns a handle to a device context. The handle is used by the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxprintcoverpagea">FaxPrintCoverPage</a> function, and by the <a href="/windows/desktop/api/wingdi/nf-wingdi-abortdoc">AbortDoc</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-enddoc">EndDoc</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-startpage">StartPage</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-endpage">EndPage</a> and other Win32 Windows Graphics Device Interface (GDI) functions.

<div class="alert"><b>Note</b>  The application must also call the <a href="/windows/desktop/api/wingdi/nf-wingdi-abortdoc">AbortDoc</a> function or the <a href="/windows/desktop/api/wingdi/nf-wingdi-enddoc">EndDoc</a> function to complete the print job, and call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a> function to deallocate the handle to the printer device context. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-printing-a-fax-to-a-device-context">Printing a Fax to a Device Context</a>.</div>
<div> </div>
A fax client application should not call the <a href="/windows/desktop/api/wingdi/nf-wingdi-createdca">CreateDC</a> GDI function to create the fax printer device context; nor should it call the <a href="/windows/desktop/api/wingdi/nf-wingdi-startpage">StartPage</a> printing function to start a fax print job. Instead, the application should call the <b>FaxStartPrintJob</b> function. This is because <b>FaxStartPrintJob</b> modifies information in the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure specific to the fax printer of interest.

The change prevents the display of the Fax Send Wizard that collects information from the user. The fax server uses the data in the <a href="/windows/desktop/api/winfax/ns-winfax-fax_print_infoa">FAX_PRINT_INFO</a> structure pointed to by the <i>PrintInfo</i> parameter to print the fax transmission. This structure contains data the Fax Send Wizard would have collected, had the wizard been displayed.

A fax client application must call the <b>FaxStartPrintJob</b> function before calling the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxprintcoverpagea">FaxPrintCoverPage</a> function to print a cover page with a fax job.





> [!NOTE]
> The winfax.h header defines FaxStartPrintJob as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-abortdoc">AbortDoc</a>



<a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enddoc">EndDoc</a>



<a href="/windows/desktop/api/winfax/ns-winfax-fax_context_infoa">FAX_CONTEXT_INFO</a>



<a href="/windows/desktop/api/winfax/ns-winfax-fax_print_infoa">FAX_PRINT_INFO</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxprintcoverpagea">FaxPrintCoverPage</a>
