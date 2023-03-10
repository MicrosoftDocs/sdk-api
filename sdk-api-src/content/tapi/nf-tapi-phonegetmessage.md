---
UID: NF:tapi.phoneGetMessage
title: phoneGetMessage function (tapi.h)
description: The phoneGetMessage function returns the next TAPI message that is queued for delivery to an application that is using the Event Handle notification mechanism (see phoneInitializeEx for further details).
helpviewer_keywords: ["_tapi2_phonegetmessage","phoneGetMessage","phoneGetMessage function [TAPI 2.2]","tapi/phoneGetMessage","tapi2.phonegetmessage"]
old-location: tapi2\phonegetmessage.htm
tech.root: tapi3
ms.assetid: 8afa17ef-a47f-41af-b120-1e2d5acb4106
ms.date: 12/05/2018
ms.keywords: _tapi2_phonegetmessage, phoneGetMessage, phoneGetMessage function [TAPI 2.2], tapi/phoneGetMessage, tapi2.phonegetmessage
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
 - phoneGetMessage
 - tapi/phoneGetMessage
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
 - phoneGetMessage
---

# phoneGetMessage function


## -description

The 
<b>phoneGetMessage</b> function returns the next TAPI message that is queued for delivery to an application that is using the Event Handle notification mechanism (see 
<a href="/windows/desktop/api/tapi/nf-tapi-phoneinitializeexa">phoneInitializeEx</a> for further details).

## -parameters

### -param hPhoneApp

Handle returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-phoneinitializeexa">phoneInitializeEx</a>. The application must have set the PHONEINITIALIZEEXOPTION_USEEVENT option in the <b>dwOptions</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-phoneinitializeexparams">PHONEINITIALIZEEXPARAMS</a> structure.

### -param lpMessage

Pointer to a 
<a href="/windows/desktop/api/tapi/ns-tapi-phonemessage">PHONEMESSAGE</a> structure. Upon successful return from this function, the structure contains the next message that had been queued for delivery to the application.

### -param dwTimeout

Time-out interval, in milliseconds. The function returns if the interval elapses, even if no message can be returned. If <i>dwTimeout</i> is zero, the function checks for a queued message and returns immediately. If <i>dwTimeout</i> is INFINITE, the function's time-out interval never elapses.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALAPPHANDLE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPOINTER, PHONEERR_NOMEM.

## -remarks

If this function has been called with a nonzero timeout and the application calls 
<a href="/windows/desktop/api/tapi/nf-tapi-phoneshutdown">phoneShutdown</a> on another thread, this function returns immediately with PHONEERR_INVALAPPHANDLE.

If the timeout expires (or was zero) and no message could be fetched from the queue, the function returns with the error PHONEERR_OPERATIONFAILED.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phoneinitializeexparams">PHONEINITIALIZEEXPARAMS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-phonemessage">PHONEMESSAGE</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phoneinitializeexa">phoneInitializeEx</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phoneshutdown">phoneShutdown</a>