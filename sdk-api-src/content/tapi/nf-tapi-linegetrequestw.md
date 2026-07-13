---
UID: NF:tapi.lineGetRequestW
title: lineGetRequestW function (tapi.h)
description: The lineGetRequestW (Unicode) function (tapi.h) retrieves the next by-proxy request for the specified request mode.
helpviewer_keywords: ["_tapi2_linegetrequest", "lineGetRequest", "lineGetRequest function [TAPI 2.2]", "lineGetRequestW", "tapi/lineGetRequest", "tapi/lineGetRequestW", "tapi2.linegetrequest"]
old-location: tapi2\linegetrequest.htm
tech.root: tapi3
ms.assetid: c72ed61f-abbe-4a6d-9f8d-95afbd5dfb04
ms.date: 08/09/2022
ms.keywords: _tapi2_linegetrequest, lineGetRequest, lineGetRequest function [TAPI 2.2], lineGetRequestA, lineGetRequestW, tapi/lineGetRequest, tapi/lineGetRequestA, tapi/lineGetRequestW, tapi2.linegetrequest
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetRequestW (Unicode) and lineGetRequestA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineGetRequestW
 - tapi/lineGetRequestW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineGetRequest
 - lineGetRequestA
 - lineGetRequestW
---

# lineGetRequestW function


## -description

The 
<b>lineGetRequest</b> function retrieves the next by-proxy request for the specified request mode.

## -parameters

### -param hLineApp

The application usage handle for the line portion of TAPI.

### -param dwRequestMode

A type of request to be obtained. Be aware that <i>dwRequestMode</i> can only have one bit set. This parameter uses one and only one of the 
<a href="/windows/desktop/Tapi/linerequestmode--constants">LINEREQUESTMODE_ Constants</a>.

### -param lpRequestBuffer

A pointer to a memory buffer where the parameters of the request are to be placed. The size of the buffer and the interpretation of the data placed in the buffer depends on the request mode. The application-allocated buffer is assumed to be of sufficient size to hold the request.

If <i>dwRequestMode</i> is LINEREQUESTMODE_MAKECALL, interpret the content of the request buffer using the 
<a href="/windows/desktop/api/tapi/ns-tapi-linereqmakecall">LINEREQMAKECALL</a> structure.

LINEREQUESTMODE_MEDIACALL is obsolete.  For more information, see tapiRequestMediaCall.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

<b>LINEERR_INVALAPPHANDLE</b>, <b>LINEERR_NOTREGISTERED</b>, <b>LINEERR_INVALPOINTER</b>, <b>LINEERR_OPERATIONFAILED</b>, <b>LINEERR_INVALREQUESTMODE</b>, <b>LINEERR_RESOURCEUNAVAIL</b>, <b>LINEERR_NOMEM</b>, <b>LINEERR_UNINITIALIZED</b>, <b>LINEERR_NOREQUEST</b>.

## -remarks

A telephony-enabled application can request that a call be placed on its behalf by invoking 
<a href="/windows/desktop/api/tapi/nf-tapi-tapirequestmakecall">tapiRequestMakeCall</a>. These requests are queued by TAPI and the highest priority application that has registered to handle the request is sent a 
<a href="/windows/desktop/Tapi/line-request">LINE_REQUEST</a> message with indication of the mode of the request that is pending. Typically, this application is the user's call-control application. The LINE_REQUEST message indicates that zero or more requests may be pending for the registered application to process; after receiving LINE_REQUEST, it is the responsibility of the recipient application to call 
<b>lineGetRequest</b> until LINEERR_NOREQUEST is returned, indicating that no more requests are pending.

Next, the call-control application that receives this message invokes 
<b>lineGetRequest</b>, specifying the request mode and a buffer that is large enough to hold the request. The call-control application then interprets and executes the request.

After execution of 
<b>lineGetRequest</b>, TAPI purges the request from its internal queue, making room available for a subsequent request. It is therefore possible for a new 
<a href="/windows/desktop/Tapi/line-request">LINE_REQUEST</a> message to be received immediately upon execution of 
<b>lineGetRequest</b>, should the same or another application issue another request. It is the responsibility of the request recipient application to handle this scenario by some mechanism; for example, by noting the additional LINE_REQUEST and deferring a subsequent 
<b>lineGetRequest</b> until processing of the preceding request completes, by getting the subsequent request and buffer as necessary, or by another appropriate means.

The subsequent LINE_REQUEST should not be ignored because it is not repeated by TAPI.





> [!NOTE]
> The tapi.h header defines lineGetRequest as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linereqmakecall">LINEREQMAKECALL</a>



<a href="/windows/desktop/Tapi/line-request">LINE_REQUEST</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-tapirequestmakecall">tapiRequestMakeCall</a>
