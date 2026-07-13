---
UID: NF:winfax.FaxSendDocumentW
title: FaxSendDocumentW function (winfax.h)
description: A fax client application calls the FaxSendDocument function to queue a fax job that will transmit an outgoing fax transmission. (Unicode)
helpviewer_keywords: ["FaxSendDocument", "FaxSendDocument function [Fax Service]", "FaxSendDocumentW", "_mfax_faxsenddocument", "fax._mfax_faxsenddocument", "winfax/FaxSendDocument", "winfax/FaxSendDocumentW"]
old-location: fax\_mfax_faxsenddocument.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7t6c.htm
ms.date: 12/05/2018
ms.keywords: FaxSendDocument, FaxSendDocument function [Fax Service], FaxSendDocumentA, FaxSendDocumentW, _mfax_faxsenddocument, fax._mfax_faxsenddocument, winfax/FaxSendDocument, winfax/FaxSendDocumentA, winfax/FaxSendDocumentW
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxSendDocumentW (Unicode) and FaxSendDocumentA (ANSI)
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
 - FaxSendDocumentW
 - winfax/FaxSendDocumentW
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
 - FaxSendDocument
 - FaxSendDocumentA
 - FaxSendDocumentW
---

# FaxSendDocumentW function


## -description

A fax client application calls the <b>FaxSendDocument</b> function to queue a fax job that will transmit an outgoing fax transmission.

## -parameters

### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function.

### -param FileName [in]

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that contains the fully qualified path and name of the file that contains the fax document to transmit. The path can be a UNC path or a path that begins with a drive letter. 

                    

This parameter can contain any valid local file name. The file must be a properly registered file type, and the fax server must be able to access the file.

### -param JobParams [in]

Type: <b>PFAX_JOB_PARAM</b>

Pointer to a <a href="/windows/desktop/api/winfax/ns-winfax-fax_job_parama">FAX_JOB_PARAM</a> structure that contains the information necessary for the fax server to send the fax transmission. The structure includes, among other items, the recipient's fax number, sender and recipient data, an optional billing code, and job scheduling information.

### -param CoverpageInfo [in, optional]

Type: <b>const <a href="/windows/desktop/api/winfax/ns-winfax-fax_coverpage_infoa">FAX_COVERPAGE_INFO</a>*</b>

Pointer to a <a href="/windows/desktop/api/winfax/ns-winfax-fax_coverpage_infoa">FAX_COVERPAGE_INFO</a> structure that contains personal data to display on the cover page of the fax document. This parameter must be <b>NULL</b> if a cover page is not required.

### -param FaxJobId [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive a unique number that identifies the queued job that will send the fax transmission.

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
One or all of the <i>FaxHandle</i>, <i>JobParams</i>, or <i>FileName</i> parameters are <b>NULL</b>; the call handle specified by the <b>CallHandle</b> member of the <a href="/windows/desktop/api/winfax/ns-winfax-fax_job_parama">FAX_JOB_PARAM</a> structure is invalid (should be <b>NULL</b>), or the <b>RecipientNumber</b> member in the <b>FAX_JOB_PARAM</b> structure is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
The <i>FaxHandle</i> parameter specifies a remote connection, but the <b>CallHandle</b> member of the <a href="/windows/desktop/api/winfax/ns-winfax-fax_job_parama">FAX_JOB_PARAM</a> structure is not <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. <a href="/previous-versions/windows/desktop/fax/-mfax-specific-fax-access-rights">FAX_JOB_SUBMIT</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The fax server cannot locate the file specified by the <i>FileName</i> or the <i>CoverpageInfo</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The fax server cannot process the file specified by the <i>FileName</i> or the <i>CoverpageInfo</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
An attempt was made to hand off a voice call to send a fax, using the <b>CallHandle</b> member of the <a href="/windows/desktop/api/winfax/ns-winfax-fax_job_parama">FAX_JOB_PARAM</a> structure. This functionality is not supported.

</td>
</tr>
</table>

## -remarks

Call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxcompletejobparamsa">FaxCompleteJobParams</a> function before calling the FaxSendDocument function. <b>FaxCompleteJobParams</b> is a utility function that fills in multiple members in the <a href="/windows/desktop/api/winfax/ns-winfax-fax_coverpage_infoa">FAX_COVERPAGE_INFO</a> and <a href="/windows/desktop/api/winfax/ns-winfax-fax_job_parama">FAX_JOB_PARAM</a> structures, with information such as the sender's name, the fax number, and optional billing code information.

The <b>FaxSendDocument</b> function executes asynchronously, and the function returns immediately. The fax server queues the job to send the fax transmission according to the details specified by the <a href="/windows/desktop/api/winfax/ns-winfax-fax_job_parama">FAX_JOB_PARAM</a> structure.

For <b>FaxSendDocument</b> to succeed, there must be a remote fax printer installed on the fax server.

To send a fax document efficiently to multiple recipients, an application should call the <b>FaxSendDocument</b> function multiple times. The <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumentforbroadcasta">FaxSendDocumentForBroadcast</a> function is supported for backward compatibility.

When you send a document from an application, links in the document may cause a dialog to appear, requesting information. If you do not handle the information request within several minutes, <b>FaxSendDocument</b> will fail and return an error.





> [!NOTE]
> The winfax.h header defines FaxSendDocument as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winfax/ns-winfax-fax_coverpage_infoa">FAX_COVERPAGE_INFO</a>



<a href="/windows/desktop/api/winfax/ns-winfax-fax_job_parama">FAX_JOB_PARAM</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxcompletejobparamsa">FaxCompleteJobParams</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumentforbroadcasta">FaxSendDocumentForBroadcast</a>
