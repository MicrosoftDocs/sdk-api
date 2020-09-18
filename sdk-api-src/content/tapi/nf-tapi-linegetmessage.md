---
UID: NF:tapi.lineGetMessage
title: lineGetMessage function (tapi.h)
description: The lineGetMessage function returns the next TAPI message that is queued for delivery to an application that is using the Event Handle notification mechanism (see lineInitializeEx for further details).
helpviewer_keywords: ["_tapi2_linegetmessage","lineGetMessage","lineGetMessage function [TAPI 2.2]","tapi/lineGetMessage","tapi2.linegetmessage"]
old-location: tapi2\linegetmessage.htm
tech.root: tapi3
ms.assetid: ed6df53e-b01d-40bc-8676-b0f7e0eacfd1
ms.date: 12/05/2018
ms.keywords: _tapi2_linegetmessage, lineGetMessage, lineGetMessage function [TAPI 2.2], tapi/lineGetMessage, tapi2.linegetmessage
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
 - lineGetMessage
 - tapi/lineGetMessage
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
 - lineGetMessage
---

# lineGetMessage function


## -description

The 
<b>lineGetMessage</b> function returns the next TAPI message that is queued for delivery to an application that is using the Event Handle notification mechanism (see 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a> for further details).

## -parameters

### -param hLineApp

Handle returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>. The application must have set the LINEINITIALIZEEXOPTION_USEEVENT option in the <b>dwOptions</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineinitializeexparams">LINEINITIALIZEEXPARAMS</a> structure.

### -param lpMessage

Pointer to a 
<a href="/windows/desktop/api/tapi/ns-tapi-linemessage">LINEMESSAGE</a> structure. Upon successful return from this function, the structure contains the next message that had been queued for delivery to the application.

### -param dwTimeout

Time-out interval, in milliseconds. The function returns if the interval elapses, even if no message can be returned. If <i>dwTimeout</i> is zero, the function checks for a queued message and returns immediately. If <i>dwTimeout</i> is INFINITE, the function's time-out interval never elapses.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALAPPHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALPOINTER, LINEERR_NOMEM.

## -remarks

If the 
<b>lineGetMessage</b> function has been called with a non-zero timeout and the application calls 
<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a> on another thread, this function returns immediately with LINEERR_INVALAPPHANDLE.

If the timeout expires (or was zero) and no message could be fetched from the queue, the function returns with the error LINEERR_OPERATIONFAILED.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineinitializeexparams">LINEINITIALIZEEXPARAMS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linemessage">LINEMESSAGE</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a>