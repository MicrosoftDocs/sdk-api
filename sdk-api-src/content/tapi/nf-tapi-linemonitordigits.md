---
UID: NF:tapi.lineMonitorDigits
title: lineMonitorDigits function (tapi.h)
description: The lineMonitorDigits function enables and disables the unbuffered detection of digits received on the call. Each time a digit of the specified digit mode is detected, a message is sent to the application indicating which digit has been detected.
helpviewer_keywords: ["_tapi2_linemonitordigits","lineMonitorDigits","lineMonitorDigits function [TAPI 2.2]","tapi/lineMonitorDigits","tapi2.linemonitordigits"]
old-location: tapi2\linemonitordigits.htm
tech.root: tapi3
ms.assetid: 7987761f-429c-4a6f-876b-eafe4274907a
ms.date: 12/05/2018
ms.keywords: _tapi2_linemonitordigits, lineMonitorDigits, lineMonitorDigits function [TAPI 2.2], tapi/lineMonitorDigits, tapi2.linemonitordigits
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
 - lineMonitorDigits
 - tapi/lineMonitorDigits
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
 - lineMonitorDigits
---

# lineMonitorDigits function


## -description

The 
<b>lineMonitorDigits</b> function enables and disables the unbuffered detection of digits received on the call. Each time a digit of the specified digit mode is detected, a message is sent to the application indicating which digit has been detected.

## -parameters

### -param hCall

Handle to the call on which digits are to be detected. The call state of <i>hCall</i> can be any state except <i>idle</i> or <i>disconnected</i>.

### -param dwDigitModes

Digit mode or modes that are to be monitored. If <i>dwDigitModes</i> is zero, digit monitoring is canceled. This parameter uses one or more of the 
<a href="/windows/desktop/Tapi/linedigitmode--constants">LINEDIGITMODE_ Constants</a>.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALDIGITMODE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.

## -remarks

This function is considered successful if digit monitoring has been correctly initiated, not when digit monitoring has terminated. Digit monitoring remains in effect until it is explicitly disabled by calling 
<b>lineMonitorDigits</b> with <i>dwDigitModes</i> set to zero, until the call transitions to idle, or when the application deallocates its call handle for the call. Although this function can be invoked in any call state, digits are usually detected only while the call is in the <i>connected</i> state.

Each time a digit is detected, a LINE_MONITORDIGITS message is sent to the application passing the detected digit as a parameter.

An application can use 
<b>lineMonitorDigits</b> to enable or disable unbuffered digit detection. It can use 
<a href="/windows/desktop/api/tapi/nf-tapi-linegatherdigits">lineGatherDigits</a> for buffered digit detection. After buffered digit gathering is complete, a 
<a href="/windows/desktop/Tapi/line-gatherdigits">LINE_GATHERDIGITS</a> message is sent to the application. Both buffered and unbuffered digit detection can be enabled on the same call simultaneously.

Monitoring of digits on a conference call applies only to the <i>hConfCall</i>, not to the individual participating calls.

## -see-also

<a href="/windows/desktop/Tapi/line-gatherdigits">LINE_GATHERDIGITS</a>



<a href="/windows/desktop/Tapi/line-monitordigits">LINE_MONITORDIGITS</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegatherdigits">lineGatherDigits</a>