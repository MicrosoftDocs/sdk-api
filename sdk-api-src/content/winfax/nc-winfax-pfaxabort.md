---
UID: NC:winfax.PFAXABORT
title: PFAXABORT (winfax.h)
description: A fax client application calls the FaxAbort function to terminate a fax job.
helpviewer_keywords: ["FaxAbortA","FaxAbortW","PFAXABORT","PFAXABORT callback","PFAXABORT callback function [Fax Service]","_mfax_faxabort","fax._mfax_faxabort","winfax/FaxAbortA","winfax/FaxAbortW","winfax/PFAXABORT"]
old-location: fax\_mfax_faxabort.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_03jo.htm
ms.date: 12/05/2018
ms.keywords: FaxAbortA, FaxAbortW, PFAXABORT, PFAXABORT callback, PFAXABORT callback function [Fax Service], _mfax_faxabort, fax._mfax_faxabort, winfax/FaxAbortA, winfax/FaxAbortW, winfax/PFAXABORT
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxAbortW (Unicode) and FaxAbortA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFAXABORT
 - winfax/PFAXABORT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winfax.h
api_name:
 - PFAXABORT
 - FaxAbortA
 - FaxAbortW
---

# PFAXABORT callback function


## -description

A fax client application calls the <b>FaxAbort</b> function to terminate a fax job.

## -parameters

### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function.

### -param JobId [in]

Type: <b>DWORD</b>

Specifies a unique number that identifies the fax job to terminate.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. You must own the job, or have <a href="/previous-versions/windows/desktop/fax/-mfax-specific-fax-access-rights">FAX_JOB_MANAGE</a> access.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>FaxHandle</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>JobId</i> parameter is invalid.

</td>
</tr>
</table>

## -remarks

An application typically calls the <b>FaxAbort</b> function to terminate a fax transmission that is in progress. To manage a queued fax job, an application typically calls the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetjoba">FaxSetJob</a> function. <b>FaxSetJob</b> can cancel an active job; the function can also pause, resume, cancel, or restart a queued fax job.

Call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumjobsa">FaxEnumJobs</a> function to retrieve a valid value to use in the <i>JobId</i> parameter.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-modifying-a-fax-job">Modifying a Fax Job</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-terminating-a-fax-job">Terminating a Fax Job</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumjobsa">FaxEnumJobs</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumenta">FaxSendDocument</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetjoba">FaxSetJob</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxstartprintjoba">FaxStartPrintJob</a>