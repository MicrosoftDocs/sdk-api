---
UID: NF:winfax.FaxPrintCoverPageA
title: FaxPrintCoverPageA function (winfax.h)
description: The FaxPrintCoverPage function prints a fax transmission cover page to the specified device context for a fax client application. (ANSI)
helpviewer_keywords: ["FaxPrintCoverPageA", "winfax/FaxPrintCoverPageA"]
old-location: fax\_mfax_faxprintcoverpage.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8fmt.htm
ms.date: 12/05/2018
ms.keywords: FaxPrintCoverPage, FaxPrintCoverPage function [Fax Service], FaxPrintCoverPageA, FaxPrintCoverPageW, _mfax_faxprintcoverpage, fax._mfax_faxprintcoverpage, winfax/FaxPrintCoverPage, winfax/FaxPrintCoverPageA, winfax/FaxPrintCoverPageW
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxPrintCoverPageW (Unicode) and FaxPrintCoverPageA (ANSI)
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
 - FaxPrintCoverPageA
 - winfax/FaxPrintCoverPageA
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
 - FaxPrintCoverPage
 - FaxPrintCoverPageA
 - FaxPrintCoverPageW
---

# FaxPrintCoverPageA function


## -description

The <b>FaxPrintCoverPage</b> function prints a fax transmission cover page to the specified device context for a fax client application.

## -parameters

### -param FaxContextInfo [in]

Type: <b>const <a href="/windows/desktop/api/winfax/ns-winfax-fax_context_infoa">FAX_CONTEXT_INFO</a>*</b>

Pointer to a <a href="/windows/desktop/api/winfax/ns-winfax-fax_context_infoa">FAX_CONTEXT_INFO</a> structure that contains a handle to a fax printer device context.

### -param CoverPageInfo [in]

Type: <b>const <a href="/windows/desktop/api/winfax/ns-winfax-fax_coverpage_infoa">FAX_COVERPAGE_INFO</a>*</b>

Pointer to a <a href="/windows/desktop/api/winfax/ns-winfax-fax_coverpage_infoa">FAX_COVERPAGE_INFO</a> structure that contains personal data to display on the cover page of the fax document.

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
One or both of the <i>CoverPageInfo</i> or <i>FaxContextInfo</i> parameters are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <b>SizeOfStruct</b> member of the specified <a href="/windows/desktop/api/winfax/ns-winfax-fax_coverpage_infoa">FAX_COVERPAGE_INFO</a> structure is not equal to <b>sizeof(FAX_COVERPAGE_INFO)</b>; or the <b>SizeOfStruct</b> member of the specified <a href="/windows/desktop/api/winfax/ns-winfax-fax_context_infoa">FAX_CONTEXT_INFO</a> structure is not equal to <b>sizeof(FAX_CONTEXT_INFO)</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The fax server cannot locate the file specified by the <b>CoverPageName</b> member of the <a href="/windows/desktop/api/winfax/ns-winfax-fax_coverpage_infoa">FAX_COVERPAGE_INFO</a> structure.

</td>
</tr>
</table>

## -remarks

A device context handle is obtained by using the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxstartprintjoba">FaxStartPrintJob</a> function.

The cover page can be a personal cover page stored on the local computer, or it can be a common cover page stored on the fax server.

<div class="alert"><b>Note</b>  The application must also call the <a href="/windows/desktop/api/wingdi/nf-wingdi-abortdoc">AbortDoc</a> function or the <a href="/windows/desktop/api/wingdi/nf-wingdi-enddoc">EndDoc</a> function to complete the print job, and call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a> function to deallocate the handle to the printer device context. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-printing-a-fax-to-a-device-context">Printing a Fax to a Device Context</a>.</div>
<div> </div>
A fax client application must call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxstartprintjoba">FaxStartPrintJob</a> function before calling the <b>FaxPrintCoverPage</b> function to print a cover page with a fax job. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-cover-pages">Cover Pages</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-printing-a-fax-to-a-device-context">Printing a Fax to a Device Context</a>.





> [!NOTE]
> The winfax.h header defines FaxPrintCoverPage as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winfax/ns-winfax-fax_context_infoa">FAX_CONTEXT_INFO</a>



<a href="/windows/desktop/api/winfax/ns-winfax-fax_coverpage_infoa">FAX_COVERPAGE_INFO</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxstartprintjoba">FaxStartPrintJob</a>
