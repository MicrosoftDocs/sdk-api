---
UID: NF:tspi.TSPI_lineAccept
title: TSPI_lineAccept function (tspi.h)
description: The TSPI_lineAccept function accepts the specified offered call. It can optionally send the specified user-user information to the calling party.
helpviewer_keywords: ["TSPI_lineAccept","TSPI_lineAccept function [TAPI 2.2]","_tspi_tspi_lineaccept","tspi.tspi_lineaccept","tspi/TSPI_lineAccept"]
old-location: tspi\tspi_lineaccept.htm
tech.root: tapi3
ms.assetid: 2690992b-b155-4ae9-816a-e5fafaffa033
ms.date: 12/05/2018
ms.keywords: TSPI_lineAccept, TSPI_lineAccept function [TAPI 2.2], _tspi_tspi_lineaccept, tspi.tspi_lineaccept, tspi/TSPI_lineAccept
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
 - TSPI_lineAccept
 - tspi/TSPI_lineAccept
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
 - TSPI_lineAccept
---

# TSPI_lineAccept function


## -description

The 
<b>TSPI_lineAccept</b> function accepts the specified offered call. It can optionally send the specified user-user information to the calling party.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdCall

The handle to the call to be accepted. The call state of <i>hdCall</i> can be <i>offering</i>.

### -param lpsUserUserInfo

A pointer to a <b>null</b>-terminated Unicode string containing user-user information to be sent to the remote party as part of the call accept. This pointer is <b>NULL</b> if no user-user information is to be sent. User-user information is only sent if supported by the underlying network (see 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>).

### -param dwSize

The size in bytes of the user-user information in <i>lpsUserUserInfo</i>. If <i>lpsUserUserInfo</i> is <b>NULL</b>, <i>dwSize</i> is ignored.

## -returns

Returns <i>dwRequestID</i> if the function is completed asynchronously or an error number if an error occurs. The <i>lResult</i> parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSTATE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_USERUSERINFOTOOBIG, LINEERR_OPERATIONUNAVAIL.

## -remarks

The 
<b>TSPI_lineAccept</b> function is used in telephony environments (such as ISDN) that allow alerting associated with incoming calls to be separate from the initial offering of the call. When a call comes in, the call is first offered. For some small time duration, the client application may have the option to reject the call using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linedrop">TSPI_lineDrop</a>, redirect the call to another station using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineredirect">TSPI_lineRedirect</a>, answer the call using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineanswer">TSPI_lineAnswer</a>, or accept the call using 
<b>TSPI_lineAccept</b>. After a call has been successfully accepted, alerting at both the called and calling device begins, and typically the call state transitions to the <i>accepted</i> state. The service provider must set the flag LINEADDRCAPFLAGS_ACCEPTTOALERT in the <b>dwAddrCapFlags</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a> data structure if the application must call 
<b>TSPI_lineAccept</b> for alerting to begin.

To TAPI, alerting is reported using the 
<a href="/previous-versions/windows/desktop/legacy/ms725231(v=vs.85)">LINE_LINEDEVSTATE</a> message with the <i>ringing</i> indication.

<b>TSPI_lineAccept</b> may also be supported by non-ISDN service providers. The call state transition to the <i>accepted</i> state can be used by other of the TAPI clients as an indication that some application has claimed responsibility for the call and has presented the call to the user.

The client application has the option to send user-user information at the time of the accept. Even if user-user information can be sent, often no guarantees are made that the network will deliver this information to the calling party. The client application may consult a line's device capabilities to determine whether call accept is available.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a>



<a href="/previous-versions/windows/desktop/legacy/ms725231(v=vs.85)">LINE_LINEDEVSTATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineanswer">TSPI_lineAnswer</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linedrop">TSPI_lineDrop</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineopen">TSPI_lineOpen</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineredirect">TSPI_lineRedirect</a>