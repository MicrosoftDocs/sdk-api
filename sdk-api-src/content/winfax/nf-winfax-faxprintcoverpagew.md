---
UID: NF:winfax.FaxPrintCoverPageW
title: FaxPrintCoverPageW function
author: windows-sdk-content
description: The FaxPrintCoverPage function prints a fax transmission cover page to the specified device context for a fax client application.
old-location: fax\_mfax_faxprintcoverpage.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8fmt.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxPrintCoverPage, FaxPrintCoverPage function [Fax Service], FaxPrintCoverPageA, FaxPrintCoverPageW, _mfax_faxprintcoverpage, fax._mfax_faxprintcoverpage, winfax/FaxPrintCoverPage, winfax/FaxPrintCoverPageA, winfax/FaxPrintCoverPageW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: EVT_VARIANT, *PEVT_VARIANT
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
product: Windows
targetos: Windows
req.lib: WinFax.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# FaxPrintCoverPageW function


## -description


The <b>FaxPrintCoverPage</b> function prints a fax transmission cover page to the specified device context for a fax client application.


## -parameters




### -param FaxContextInfo [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms692352(v=VS.85).aspx">FAX_CONTEXT_INFO</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms692352(v=VS.85).aspx">FAX_CONTEXT_INFO</a> structure that contains a handle to a fax printer device context.


### -param CoverPageInfo [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms691508(v=VS.85).aspx">FAX_COVERPAGE_INFO</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms691508(v=VS.85).aspx">FAX_COVERPAGE_INFO</a> structure that contains personal data to display on the cover page of the fax document.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. GetLastError can return one of the following errors.

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
The <b>SizeOfStruct</b> member of the specified <a href="https://msdn.microsoft.com/en-us/library/ms691508(v=VS.85).aspx">FAX_COVERPAGE_INFO</a> structure is not equal to <b>sizeof(FAX_COVERPAGE_INFO)</b>; or the <b>SizeOfStruct</b> member of the specified <a href="https://msdn.microsoft.com/en-us/library/ms692352(v=VS.85).aspx">FAX_CONTEXT_INFO</a> structure is not equal to <b>sizeof(FAX_CONTEXT_INFO)</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The fax server cannot locate the file specified by the <b>CoverPageName</b> member of the <a href="https://msdn.microsoft.com/en-us/library/ms691508(v=VS.85).aspx">FAX_COVERPAGE_INFO</a> structure.

</td>
</tr>
</table>
 




## -remarks



A device context handle is obtained by using the <a href="https://msdn.microsoft.com/en-us/library/ms691423(v=VS.85).aspx">FaxStartPrintJob</a> function.

The cover page can be a personal cover page stored on the local computer, or it can be a common cover page stored on the fax server.

<div class="alert"><b>Note</b>  The application must also call the <a href="https://msdn.microsoft.com/en-us/library/Dd162456(v=VS.85).aspx">AbortDoc</a> function or the <a href="https://msdn.microsoft.com/en-us/library/Dd162594(v=VS.85).aspx">EndDoc</a> function to complete the print job, and call the <a href="https://msdn.microsoft.com/en-us/library/Dd183533(v=VS.85).aspx">DeleteDC</a> function to deallocate the handle to the printer device context. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690908(v=VS.85).aspx">Printing a Fax to a Device Context</a>.</div>
<div> </div>
A fax client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms691423(v=VS.85).aspx">FaxStartPrintJob</a> function before calling the <b>FaxPrintCoverPage</b> function to print a cover page with a fax job. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms691363(v=VS.85).aspx">Cover Pages</a> and <a href="https://msdn.microsoft.com/en-us/library/ms690908(v=VS.85).aspx">Printing a Fax to a Device Context</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms692352(v=VS.85).aspx">FAX_CONTEXT_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691508(v=VS.85).aspx">FAX_COVERPAGE_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691947(v=VS.85).aspx">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691423(v=VS.85).aspx">FaxStartPrintJob</a>
 

 

