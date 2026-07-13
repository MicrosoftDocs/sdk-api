---
UID: NF:tapi.lineAccept
title: lineAccept function (tapi.h)
description: The lineAccept function accepts the specified offered call. It can optionally send the specified user-user information to the calling party.
helpviewer_keywords: ["_tapi2_lineaccept","lineAccept","lineAccept function [TAPI 2.2]","tapi/lineAccept","tapi2.lineaccept"]
old-location: tapi2\lineaccept.htm
tech.root: tapi3
ms.assetid: 185f129a-ba8c-496b-ab1a-ba22e5928c54
ms.date: 12/05/2018
ms.keywords: _tapi2_lineaccept, lineAccept, lineAccept function [TAPI 2.2], tapi/lineAccept, tapi2.lineaccept
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
 - lineAccept
 - tapi/lineAccept
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
 - lineAccept
---

# lineAccept function


## -description

The 
<b>lineAccept</b> function accepts the specified offered call. It can optionally send the specified user-user information to the calling party.

## -parameters

### -param hCall

Handle to the call to be accepted. The application must be an owner of the call. Call state of <i>hCall</i> must be <i>offering</i>.

### -param lpsUserUserInfo

Pointer to a <b>null</b>-terminated string containing user-user information to be sent to the remote party as part of the call accept. This pointer can be left <b>NULL</b> if no user-user information is to be sent. User-user information is only sent if supported by the underlying network (see 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>). The protocol discriminator member for the user-user information, if required, should appear as the first byte of the buffer pointed to by <i>lpsUserUserInfo</i>, and must be accounted for in <i>dwSize</i>.

### -param dwSize

Size of the user-user information in <i>lpsUserUserInfo</i> (including the <b>null</b> terminator), in bytes. If <i>lpsUserUserInfo</i> is <b>NULL</b>, no user-user information is sent to the calling party and <i>dwSize</i> is ignored.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds, or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_INVALCALLSTATE, LINEERR_INVALPOINTER, LINEERR_NOMEM, LINEERR_NOTOWNER, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED, LINEERR_USERUSERINFOTOOBIG.

## -remarks

The 
<b>lineAccept</b> function is used in telephony environments like Integrated Services Digital Network (ISDN) that allow alerting associated with incoming calls to be separate from the initial offering of the call. When a call comes in, it is first offered. For some small amount of time, the application may have the option to reject the call using 
<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a>, redirect the call to another station using 
<a href="/windows/desktop/api/tapi/nf-tapi-lineredirect">lineRedirect</a>, answer the call using 
<a href="/windows/desktop/api/tapi/nf-tapi-lineanswer">lineAnswer</a>, or accept the call using 
<b>lineAccept</b>. After a call has been successfully accepted by an application, alerting begins at both the called and calling device and the call state typically transitions to <i>accepted</i>.

Alerting is reported to the application by the 
<a href="/windows/desktop/Tapi/line-linedevstate">LINE_LINEDEVSTATE</a> message with the <i>ringing</i> indication.

The 
<b>lineAccept</b> function may also be supported by non-ISDN service providers. The call state transition to accepted can be used by other applications as an indication that another application has claimed responsibility for the call and has presented the call to the user.

The application has the option to send user-user information at the time of the accept. Even if user-user information is sent, there is no guarantee that the network will deliver this information to the calling party. An application should consult a line's device capabilities to determine whether call accept is available.

## -see-also

<a href="/windows/desktop/Tapi/accept-ovr">Accept overview</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineanswer">lineAnswer</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineredirect">lineRedirect</a>