---
UID: NF:tapi.lineAnswer
title: lineAnswer function (tapi.h)
description: The lineAnswer function answers the specified offering call.
helpviewer_keywords: ["_tapi2_lineanswer","lineAnswer","lineAnswer function [TAPI 2.2]","tapi/lineAnswer","tapi2.lineanswer"]
old-location: tapi2\lineanswer.htm
tech.root: tapi3
ms.assetid: dd51991c-c044-4b88-8f97-9e0ae701a2a5
ms.date: 12/05/2018
ms.keywords: _tapi2_lineanswer, lineAnswer, lineAnswer function [TAPI 2.2], tapi/lineAnswer, tapi2.lineanswer
req.header: tapi.h
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineAnswer
 - tapi/lineAnswer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ras-tapi32-l1-1-1.dll
 - Tapi32.dll
api_name:
 - lineAnswer
---

# lineAnswer function


## -description

The 
<b>lineAnswer</b> function answers the specified offering call.

## -parameters

### -param hCall

Handle to the call to be answered. The application must be an owner of this call. The call state of <i>hCall</i> must be <i>offering</i> or <i>accepted</i>.

### -param lpsUserUserInfo

Pointer to a <b>null</b>-terminated string containing user-user information to be sent to the remote party at the time the call is answered. This pointer can be left <b>NULL</b> if no user-user information is to be sent. User-user information is only sent if supported by the underlying network (see 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>). The protocol discriminator field for the user-user information, if required, should appear as the first byte of the buffer pointed to by <i>lpsUserUserInfo</i>, and must be accounted for in <i>dwSize</i>.

### -param dwSize

Size of the user-user information in <i>lpsUserUserInfo</i> (including the <b>null</b> terminator), in bytes If <i>lpsUserUserInfo</i> is <b>NULL</b>, no user-user information is sent to the calling party and <i>dwSize</i> is ignored.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INUSE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSTATE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NOMEM, LINEERR_USERUSERINFOTOOBIG, LINEERR_NOTOWNER.

## -remarks

When a new call arrives, applications with an interest in the call are sent a 
<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a> message to provide the new call handle and to inform the application about the call's state and the privileges to the new call (such as monitor or owner). The application with owner privilege for the call can answer this call using 
<b>lineAnswer</b>. After the call has been successfully answered, the call typically transitions to the <i>connected</i> state. Initially, only one application is given owner privilege to the incoming call.

In some telephony environments (like ISDN), where user alerting is separate from call offering, the application can have the option to accept a call prior to answering or to reject or redirect the offering call.

If a call comes in (is offered) at the time another call is already active, invoking 
<b>lineAnswer</b> connects to the new call. The effect this has on the existing active call depends on the line's device capabilities. The first call can be unaffected, it can automatically be dropped, or it can automatically be placed on hold. The appropriate LINE_CALLSTATE messages report state transitions to the application about both calls.

In a bridged situation, if a call is connected but in the LINECONNECTEDMODE_INACTIVE state, it can be joined using the 
<b>lineAnswer</b> function.

The application has the option to send user-user information at the time of the answer. Even if user-user information can be sent, there is no guarantee that the network will deliver this information to the calling party. An application should consult a line's device capabilities to determine whether sending user-user information upon answering the call is available.

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a>



<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>