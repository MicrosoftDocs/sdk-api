---
UID: NF:tspi.TSPI_lineAnswer
title: TSPI_lineAnswer function (tspi.h)
description: The TSPI_lineAnswer function answers the specified offering call.
helpviewer_keywords: ["TSPI_lineAnswer","TSPI_lineAnswer function [TAPI 2.2]","_tspi_tspi_lineanswer","tspi.tspi_lineanswer","tspi/TSPI_lineAnswer"]
old-location: tspi\tspi_lineanswer.htm
tech.root: tapi3
ms.assetid: efd4d7f8-bf81-46c4-b51b-516036e9baef
ms.date: 12/05/2018
ms.keywords: TSPI_lineAnswer, TSPI_lineAnswer function [TAPI 2.2], _tspi_tspi_lineanswer, tspi.tspi_lineanswer, tspi/TSPI_lineAnswer
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
 - TSPI_lineAnswer
 - tspi/TSPI_lineAnswer
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
 - TSPI_lineAnswer
---

# TSPI_lineAnswer function


## -description

The 
<b>TSPI_lineAnswer</b> function answers the specified offering call.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdCall

The service provider's handle to the call to be answered. The call state of <i>hdCall</i> can be <i>offering</i> or <i>accepted</i>.

### -param lpsUserUserInfo

A pointer to a <b>null</b>-terminated string containing user-user information to be sent to the remote party at the time of answering the call. If this pointer is <b>NULL</b>, it indicates that no user-user information is to be sent. User-user information is only sent if supported by the underlying network (as indicated in 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>).

### -param dwSize

The size in bytes of the user-user information in <i>lpsUserUserInfo</i>. If <i>lpsUserUserInfo</i> is <b>NULL</b>, <i>dwSize</i> is ignored.

## -returns

Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INUSE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_USERUSERINFOTOOBIG.

## -remarks

When a new call arrives, the service provider sends TAPI a 
<a href="/windows/desktop/Tapi/line-newcall">LINE_NEWCALL</a> message to exchange handles for the call. The service provider follows this with a 
<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a> message to inform TAPI and its client applications of the call's state. A client application typically answers the call using 
<b>TSPI_lineAnswer</b>. Typically, after the call is successfully answered, the call transitions to the <i>connected</i> state.

In some telephony environments (like ISDN) where user alerting is separate from call offering, TAPI and its client applications may have the option to first accept a call prior to answering, or instead to reject or redirect the <i>offering</i> call.

If a call is offered at the time another call is already active, the new call is connected to by invoking 
<b>TSPI_lineAnswer</b>. The effect this has on the existing active call depends on the line's device capabilities. The first call may be unaffected, it may automatically be dropped, or it may automatically be placed on hold. The appropriate LINE_CALLSTATE messages are used to report state transitions to TAPI about both calls.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a>



<a href="/windows/desktop/Tapi/line-newcall">LINE_NEWCALL</a>