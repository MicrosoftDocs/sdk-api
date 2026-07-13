---
UID: NF:winfax.FaxSendDocumentForBroadcastA
title: FaxSendDocumentForBroadcastA function (winfax.h)
description: A fax client application calls the FaxSendDocumentForBroadcast function to queue several fax jobs that will transmit the same outgoing fax transmission to several recipients. (ANSI)
helpviewer_keywords: ["FaxSendDocumentForBroadcastA", "winfax/FaxSendDocumentForBroadcastA"]
old-location: fax\_mfax_faxsenddocumentforbroadcast.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0sz8.htm
ms.date: 12/05/2018
ms.keywords: FaxSendDocumentForBroadcast, FaxSendDocumentForBroadcast function [Fax Service], FaxSendDocumentForBroadcastA, FaxSendDocumentForBroadcastW, _mfax_faxsenddocumentforbroadcast, fax._mfax_faxsenddocumentforbroadcast, winfax/FaxSendDocumentForBroadcast, winfax/FaxSendDocumentForBroadcastA, winfax/FaxSendDocumentForBroadcastW
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxSendDocumentForBroadcastW (Unicode) and FaxSendDocumentForBroadcastA (ANSI)
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
 - FaxSendDocumentForBroadcastA
 - winfax/FaxSendDocumentForBroadcastA
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
 - FaxSendDocumentForBroadcast
 - FaxSendDocumentForBroadcastA
 - FaxSendDocumentForBroadcastW
---

# FaxSendDocumentForBroadcastA function


## -description

A fax client application calls the <b>FaxSendDocumentForBroadcast</b> function to queue several fax jobs that will transmit the same outgoing fax transmission to several recipients.

## -parameters

### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function.

### -param FileName [in]

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that contains the fully qualified path and name of the file that contains the fax document to transmit to all recipients. The path can be a UNC path or a path that begins with a drive letter. 

                    



This parameter can contain any valid local file name. The file must be a properly registered file type, and the fax server must be able to access the file.

### -param FaxJobId [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the unique number that identifies the queued job that will send the fax transmission.

### -param FaxRecipientCallback [in]

Type: <b>PFAX_RECIPIENT_CALLBACK</b>

Pointer to a <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfax_recipient_callbacka">FAX_RECIPIENT_CALLBACK</a> function that retrieves user-specific information for each designated recipient of the fax transmission. The <b>FaxSendDocumentForBroadcast</b> function calls the <b>FAX_RECIPIENT_CALLBACK</b> function once for each fax recipient until it returns a value of zero, indicating that all outbound transmissions have been queued.

### -param Context [in]

Type: <b>LPVOID</b>

Pointer to a variable that contains application-specific context information or an application-defined value. <b>FaxSendDocumentForBroadcast</b> passes this data to the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfax_recipient_callbacka">FAX_RECIPIENT_CALLBACK</a> function.

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
One or all of the <i>FaxHandle</i>, <i>FileName</i>, <i>FaxRecipientCallback</i>, or <i>FaxJobId</i> parameters are <b>NULL</b>, or the <b>RecipientNumber</b> member in the <a href="/windows/desktop/api/winfax/ns-winfax-fax_job_parama">FAX_JOB_PARAM</a> structure is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The fax server cannot locate the file specified by the <i>FileName</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The fax server cannot render the file specified by the <i>FileName</i> parameter.

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
</table>

## -remarks

The function calls the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfax_recipient_callbacka">FAX_RECIPIENT_CALLBACK</a> function once for each designated fax recipient.

An application should call the <b>FaxSendDocumentForBroadcast</b> function to efficiently send a fax document to multiple recipients, rather than calling <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumenta">FaxSendDocument</a> multiple times. This is because <b>FaxSendDocumentForBroadcast</b> stores the master document only once, using the same file for all outbound transmissions.

<div class="alert"><b>Note</b>  To send a fax document efficiently to multiple recipients, an application should call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumenta">FaxSendDocument</a> function multiple times. The <b>FaxSendDocumentForBroadcast</b> function is supported for backward compatibility.</div>
<div> </div>
The <b>FaxSendDocumentForBroadcast</b> function performs the following operations in the order indicated:

<ol>
<li>The function queues the master document for transmission to multiple fax transmission recipients.</li>
<li>The function calls the user-defined <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfax_recipient_callbacka">FAX_RECIPIENT_CALLBACK</a> function. If the callback function supplies the required information for the transmission to a fax recipient, it returns a value of nonzero. This value indicates that <b>FaxSendDocumentForBroadcast</b> should use the data to queue an outbound fax.</li>
<li>The function queues a fax transmission job for the first recipient using the master document.</li>
<li>The function calls the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfax_recipient_callbacka">FAX_RECIPIENT_CALLBACK</a> function multiple times, until it returns a value of zero. Each time <b>FAX_RECIPIENT_CALLBACK</b> returns nonzero, the <b>FaxSendDocumentForBroadcast</b> function queues an outbound transmission for the next fax recipient. A value of zero indicates that there are no more fax transmission jobs to queue, and calls to <b>FAX_RECIPIENT_CALLBACK</b> should be terminated.</li>
</ol>
For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-transmitting-faxes">Transmitting Faxes</a>.





> [!NOTE]
> The winfax.h header defines FaxSendDocumentForBroadcast as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfax_recipient_callbacka">FAX_RECIPIENT_CALLBACK</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumenta">FaxSendDocument</a>
