---
UID: NF:tspi.TSPI_lineDial
title: TSPI_lineDial function (tspi.h)
description: The TSPI_lineDial function dials the specified dialable number on the specified call.
helpviewer_keywords: ["TSPI_lineDial","TSPI_lineDial function [TAPI 2.2]","_tspi_tspi_linedial","tspi.tspi_linedial","tspi/TSPI_lineDial"]
old-location: tspi\tspi_linedial.htm
tech.root: tapi3
ms.assetid: 8b24b9a3-af97-45dc-aaaf-d95ce9007ba8
ms.date: 12/05/2018
ms.keywords: TSPI_lineDial, TSPI_lineDial function [TAPI 2.2], _tspi_tspi_linedial, tspi.tspi_linedial, tspi/TSPI_lineDial
req.header: tspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - TSPI_lineDial
 - tspi/TSPI_lineDial
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineDial
---

# TSPI_lineDial function


## -description

The 
<b>TSPI_lineDial</b> function dials the specified dialable number on the specified call.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdCall

The service provider's handle to the call to be dialed. The call state of <i>hdCall</i> can be any state except <i>idle</i> and <i>disconnected</i>.

### -param lpszDestAddress

Pointer to a <b>null</b>-terminated Unicode string that specifies the destination to be dialed using the standard dialable number format.

### -param dwCountryCode

The country or region code of the destination. The implementation uses this to select the call progress protocols for the destination address. If a value of 0 is specified, a default call-progress protocol defined by the service provider is used. TAPI does not validate this parameter when this function is called.

## -returns

Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALADDRESS, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALCOUNTRYCODE, LINEERR_DIALBILLING, LINEERR_INVALCALLSTATE, LINEERR_DIALQUIET, LINEERR_ADDRESSBLOCKED, LINEERR_DIALDIALTONE, LINEERR_NOMEM, LINEERR_DIALPROMPT, LINEERR_OPERATIONUNAVAIL.

## -remarks

The service provider returns LINEERR_INVALCALLSTATE if the current state of the call does not allow dialing.

The service provider carries out no dialing if it returns LINEERR_INVALADDRESS.

If the service provider returns LINEERR_DIALBILLING, LINEERR_DIALQUIET, LINEERR_DIALDIALTONE, or LINEERR_DIALPROMPT, it should perform none of the actions otherwise performed by 
<b>TSPI_lineDial</b> (for example, no partial dialing, and no going offhook). This is because the service provider should pre-scan the number for unsupported characters first.

<b>TSPI_lineDial</b> is used for dialing on an existing call appearance; for example, call handles returned from 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemakecall">TSPI_lineMakeCall</a> with <b>NULL</b> as the <i>lpszDestAddress</i> or ending in ';', call handles returned from 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetuptransfer">TSPI_lineSetupTransfer</a> or 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetupconference">TSPI_lineSetupConference</a>. 
<b>TSPI_lineDial</b> can be invoked multiple times in the course of dialing in the case of multistage dialing, if the line's device capabilities permit it.

If the string pointed to by the <i>lpszDestAddress</i> parameter in the previous call to the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemakecall">TSPI_lineMakeCall</a> or 
<b>TSPI_lineDial</b> function is terminated with a semicolon, an empty string in the current call to 
<b>TSPI_lineDial</b> indicates that dialing is complete.

Multiple addresses can be provided in a single dial string separated by CRLF. Service providers that provide inverse multiplexing can establish individual physical calls with each of the addresses, and return a single call handle to the aggregate of all calls to the application. All addresses would use the same country or region code.

Dialing is considered complete after the address has been accepted by the service provider, not after the call is finally connected. Service providers that provide inverse multiplexing may allow multiple addresses to be provided at once. The service provider must send 
<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a> messages to TAPI to inform it about the progress of the call.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemakecall">TSPI_lineMakeCall</a>