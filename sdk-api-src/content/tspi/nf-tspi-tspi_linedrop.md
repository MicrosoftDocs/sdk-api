---
UID: NF:tspi.TSPI_lineDrop
title: TSPI_lineDrop function (tspi.h)
description: The TSPI_lineDrop function drops or disconnects the specified call.
helpviewer_keywords: ["TSPI_lineDrop","TSPI_lineDrop function [TAPI 2.2]","_tspi_tspi_linedrop","tspi.tspi_linedrop","tspi/TSPI_lineDrop"]
old-location: tspi\tspi_linedrop.htm
tech.root: tapi3
ms.assetid: ac7ec102-d7ad-4e63-833e-3c798487d7b4
ms.date: 12/05/2018
ms.keywords: TSPI_lineDrop, TSPI_lineDrop function [TAPI 2.2], _tspi_tspi_linedrop, tspi.tspi_linedrop, tspi/TSPI_lineDrop
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
 - TSPI_lineDrop
 - tspi/TSPI_lineDrop
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
 - TSPI_lineDrop
---

# TSPI_lineDrop function


## -description

The 
<b>TSPI_lineDrop</b> function drops or disconnects the specified call. User-user information can optionally be transmitted as part of the call disconnect. This function can be called by the application at any time. When 
<b>TSPI_lineDrop</b> returns, the call should be <i>idle</i>.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdCall

The service provider's handle to the call to be dropped. The call state of <i>hdCall</i> can be any state except <i>idle</i>.

### -param lpsUserUserInfo

This pointer is only valid if <b>dwSize</b> is nonzero. It specifies a pointer to a <b>null</b>-terminated string containing user-user information to be sent to the remote party as part of the call disconnect. This pointer is <b>NULL</b> if no user-user information is to be sent. User-user information is only sent if supported by the underlying network (see 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>).

### -param dwSize

The size in bytes of the user-user information in <i>lpsUserUserInfo</i>. If <i>lpsUserUserInfo</i> is <b>NULL</b>, <i>dwSize</i> is ignored.

## -returns

Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSTATE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_USERUSERINFOTOOBIG, LINEERR_OPERATIONUNAVAIL.

## -remarks

The service provider returns LINEERR_INVALCALLSTATE if the current state of the call does not allow the call to be dropped.

When invoking 
<b>TSPI_lineDrop</b>, related calls can sometimes be affected as well. For example, dropping a conference call may drop all individual participating calls. 
<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a> messages are sent to TAPI for all calls whose call state is affected. Typically, a dropped call transitions to the <i>idle</i> state. Invoking 
<b>TSPI_lineDrop</b> on a call in the <i>offering</i> state rejects the call. Not all telephone networks provide this capability.

In situations where the call to be dropped is a consultation call established during transfer or conference call establishment, the original call that was placed in the <i>OnHoldPending</i> state is reconnected to and it typically re-enters the <i>connected</i> call state.

TAPI has the option to send user-user information at the time of the drop. Even if user-user information can be sent, there is no guarantee that the network will deliver this information to the remote party.

<div class="alert"><b>Note</b>  In various bridged or party line configurations when multiple parties are on the call, 
<b>TSPI_lineDrop</b> may not actually clear the call.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetdevcaps">TSPI_lineGetDevCaps</a>