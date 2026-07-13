---
UID: NC:winfax.PFAX_RECIPIENT_CALLBACKA
title: PFAX_RECIPIENT_CALLBACKA (winfax.h)
description: The FAX_RECIPIENT_CALLBACK function is an application-defined or library-defined callback function that the FaxSendDocumentForBroadcast function calls to retrieve user-specific information for the transmission. (ANSI)
helpviewer_keywords: ["FAX_RECIPIENT_CALLBACK","FAX_RECIPIENT_CALLBACK callback","FAX_RECIPIENT_CALLBACK callback function [Fax Service]","PFAX_RECIPIENT_CALLBACKA","PFAX_RECIPIENT_CALLBACKW","_mfax_fax_recipient_callback","fax._mfax_fax_recipient_callback","winfax/FAX_RECIPIENT_CALLBACK","winfax/PFAX_RECIPIENT_CALLBACKA","winfax/PFAX_RECIPIENT_CALLBACKW"]
old-location: fax\_mfax_fax_recipient_callback.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5a5n.htm
ms.date: 12/05/2018
ms.keywords: FAX_RECIPIENT_CALLBACK, FAX_RECIPIENT_CALLBACK callback, FAX_RECIPIENT_CALLBACK callback function [Fax Service], PFAX_RECIPIENT_CALLBACKA, PFAX_RECIPIENT_CALLBACKW, _mfax_fax_recipient_callback, fax._mfax_fax_recipient_callback, winfax/FAX_RECIPIENT_CALLBACK, winfax/PFAX_RECIPIENT_CALLBACKA, winfax/PFAX_RECIPIENT_CALLBACKW
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PFAX_RECIPIENT_CALLBACKW (Unicode) and PFAX_RECIPIENT_CALLBACKA (ANSI)
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
 - PFAX_RECIPIENT_CALLBACKA
 - winfax/PFAX_RECIPIENT_CALLBACKA
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
 - FAX_RECIPIENT_CALLBACK
 - PFAX_RECIPIENT_CALLBACKA
 - PFAX_RECIPIENT_CALLBACKW
---

# PFAX_RECIPIENT_CALLBACKA callback function


## -description

The <b>FAX_RECIPIENT_CALLBACK</b> function is an application-defined or library-defined callback function that the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumentforbroadcasta">FaxSendDocumentForBroadcast</a> function calls to retrieve user-specific information for the transmission.

## -parameters

### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function.

### -param RecipientNumber [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the number of times the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumentforbroadcasta">FaxSendDocumentForBroadcast</a> function has called the <b>FAX_RECIPIENT_CALLBACK</b> function. Each function call corresponds to one designated fax recipient, and the index is relative to 1.

### -param Context [in]

Type: <b>LPVOID</b>

Pointer to a variable that contains application-specific context information or an application-defined value. <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumentforbroadcasta">FaxSendDocumentForBroadcast</a> passes this data to the <b>FAX_RECIPIENT_CALLBACK</b> function.

### -param JobParams [in, out]

Type: <b>PFAX_JOB_PARAM</b>

Pointer to a <a href="/windows/desktop/api/winfax/ns-winfax-fax_job_parama">FAX_JOB_PARAM</a> structure that contains the information necessary for the fax server to send the fax transmission to the designated recipient. The structure includes, among other items, the recipient's fax number, sender and recipient data, an optional billing code, and job scheduling information. The fax server queues the fax transmission according to the details specified by the <b>FAX_JOB_PARAM</b> structure.

### -param CoverpageInfo [in, out, optional]

Type: <b>PFAX_COVERPAGE_INFO</b>

Pointer to a <a href="/windows/desktop/api/winfax/ns-winfax-fax_coverpage_infoa">FAX_COVERPAGE_INFO</a> structure that contains cover page data to display on the cover page of the fax document for the designated recipient. This parameter must be <b>NULL</b> if a cover page is not required.

## -returns

Type: <b>BOOL</b>

The function returns a value of nonzero to indicate that the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumentforbroadcasta">FaxSendDocumentForBroadcast</a> function should queue an outbound fax transmission, using the data pointed to by the <i>JobParams</i> and <i>CoverpageInfo</i> parameters.

The function returns a value of zero to indicate that there are no more fax transmission jobs to queue, and calls to <b>FAX_RECIPIENT_CALLBACK</b> should be terminated. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumentforbroadcasta">FaxSendDocumentForBroadcast</a> calls <b>FAX_RECIPIENT_CALLBACK</b> multiple times, once for each designated fax recipient.

The <b>PFAX_RECIPIENT_CALLBACK</b> data type is a pointer to a <b>FAX_RECIPIENT_CALLBACK</b> function.

Call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxcompletejobparamsa">FaxCompleteJobParams</a> function before calling the <b>FAX_RECIPIENT_CALLBACK</b> function. <b>FaxCompleteJobParams</b> is a utility function that fills multiple members in the <a href="/windows/desktop/api/winfax/ns-winfax-fax_coverpage_infoa">FAX_COVERPAGE_INFO</a> and <a href="/windows/desktop/api/winfax/ns-winfax-fax_job_parama">FAX_JOB_PARAM</a> structures, with information such as the sender's name, fax number, and optional billing code information.

A fax client application must specify the <b>FAX_RECIPIENT_CALLBACK</b> function by passing its address when it calls the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumentforbroadcasta">FaxSendDocumentForBroadcast</a> function.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-transmitting-faxes">Transmitting Faxes</a>.





> [!NOTE]
> The winfax.h header defines PFAX_RECIPIENT_CALLBACK as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winfax/ns-winfax-fax_coverpage_infoa">FAX_COVERPAGE_INFO</a>



<a href="/windows/desktop/api/winfax/ns-winfax-fax_job_parama">FAX_JOB_PARAM</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsenddocumentforbroadcasta">FaxSendDocumentForBroadcast</a>
