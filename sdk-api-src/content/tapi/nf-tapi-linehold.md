---
UID: NF:tapi.lineHold
title: lineHold function (tapi.h)
description: The lineHold function places the specified call on hold.
helpviewer_keywords: ["_tapi2_linehold","lineHold","lineHold function [TAPI 2.2]","tapi/lineHold","tapi2.linehold"]
old-location: tapi2\linehold.htm
tech.root: tapi3
ms.assetid: d2fd450c-402c-4122-a785-a6b5216acfe9
ms.date: 12/05/2018
ms.keywords: _tapi2_linehold, lineHold, lineHold function [TAPI 2.2], tapi/lineHold, tapi2.linehold
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
 - lineHold
 - tapi/lineHold
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
 - lineHold
---

# lineHold function


## -description

The 
<b>lineHold</b> function places the specified call on hold.

## -parameters

### -param hCall

Handle to the call to be placed on hold. The application must be an owner of the call. The call state of <i>hCall</i> must be <i>connected</i>.

## -returns

Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_NOTOWNER, LINEERR_UNINITIALIZED.

## -remarks

The call on hold is temporarily disconnected allowing the application to use the line device for making or answering other calls. The 
<b>lineHold</b> function performs a so-called "hard hold" of the specified call (as opposed to a "consultation call"). A call on hard hold typically cannot be transferred or included in a conference call, but a consultation call can. Consultation calls are initiated using 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetuptransfer">lineSetupTransfer</a>, 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetupconference">lineSetupConference</a>, or 
<a href="/windows/desktop/api/tapi/nf-tapi-lineprepareaddtoconference">linePrepareAddToConference</a>.

After a call has been successfully placed on hold, the call state typically transitions to <i>onHold</i>. A held call is retrieved by 
<a href="/windows/desktop/api/tapi/nf-tapi-lineunhold">lineUnhold</a>. While a call is on hold, the application can receive 
<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a> messages about state changes of the held call. For example, if the held party hangs up, the call state can transition to <i>disconnected</i>.

In a bridged situation, a 
<b>lineHold</b> operation may possibly not actually place the call on hold, because the status of other stations on the call can govern (for example, attempting to "hold" a call when other stations are participating is not be possible); instead, the call can simply be changed to the LINECONNECTEDMODE_INACTIVE mode if it remains <i>connected</i> at other stations.

## -see-also

<a href="/windows/desktop/Tapi/hold-ovr">Hold Overview</a>



<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineprepareaddtoconference">linePrepareAddToConference</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetupconference">lineSetupConference</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetuptransfer">lineSetupTransfer</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineunhold">lineUnhold</a>