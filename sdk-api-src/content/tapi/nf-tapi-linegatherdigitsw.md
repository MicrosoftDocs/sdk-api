---
UID: NF:tapi.lineGatherDigitsW
title: lineGatherDigitsW function (tapi.h)
description: The lineGatherDigitsW (Unicode) function initiates the buffered gathering of digits on the specified call.
helpviewer_keywords: ["_tapi2_linegatherdigits", "lineGatherDigits", "lineGatherDigits function [TAPI 2.2]", "lineGatherDigitsW", "tapi/lineGatherDigits", "tapi/lineGatherDigitsW", "tapi2.linegatherdigits"]
old-location: tapi2\linegatherdigits.htm
tech.root: tapi3
ms.assetid: 87d5f777-e536-46be-8ad4-437386f04c9b
ms.date: 08/09/2022
ms.keywords: _tapi2_linegatherdigits, lineGatherDigits, lineGatherDigits function [TAPI 2.2], lineGatherDigitsA, lineGatherDigitsW, tapi/lineGatherDigits, tapi/lineGatherDigitsA, tapi/lineGatherDigitsW, tapi2.linegatherdigits
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGatherDigitsW (Unicode) and lineGatherDigitsA (ANSI)
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
 - lineGatherDigitsW
 - tapi/lineGatherDigitsW
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
 - lineGatherDigits
 - lineGatherDigitsA
 - lineGatherDigitsW
---

# lineGatherDigitsW function


## -description

The 
<b>lineGatherDigits</b> function initiates the buffered gathering of digits on the specified call. The application specifies a buffer in which to place the digits and the maximum number of digits to be collected.

## -parameters

### -param hCall

Handle to the call on which digits are to be gathered. The application must be an owner of the call. The call state of <i>hCall</i> can be any state.

### -param dwDigitModes

Digit modes to be monitored. This parameter uses one or more of the 
<a href="/windows/desktop/Tapi/linedigitmode--constants">LINEDIGITMODE_ Constants</a>.

### -param lpsDigits

Pointer to the buffer where detected digits are to be stored as text characters. Digits may not show up in the buffer one at a time as they are collected. Only after a 
<a href="/windows/desktop/Tapi/line-gatherdigits">LINE_GATHERDIGITS</a> message is received should the content of the buffer be assumed to be valid. If <i>lpsDigits</i> is <b>NULL</b>, the digit gathering currently in progress on the call is terminated and <i>dwNumDigits</i> is ignored. Otherwise, <i>lpsDigits</i> is assumed to have room for <i>dwNumDigits</i> digits.

### -param dwNumDigits

Number of digits to be collected before a LINE_GATHERDIGITS message is sent to the application. The <i>dwNumDigits</i> parameter is ignored when <i>lpsDigits</i> is <b>NULL</b>. This function fails if <i>dwNumDigits</i> is zero.

### -param lpszTerminationDigits

<b>Null</b>-terminated string of termination digits as text characters. If one of the digits in the string is detected, that termination digit is appended to the buffer, digit collection is terminated, and the 
<a href="/windows/desktop/Tapi/line-gatherdigits">LINE_GATHERDIGITS</a> message is sent to the application. 




The list of valid characters is dependent on the constant provided in <i>dwDigitModes</i>. For a list of the valid characters for each possible mode, see 
<a href="/windows/desktop/Tapi/linedigitmode--constants">LINEDIGITMODE_ Constants</a>.

If this pointer is <b>NULL</b>, or if it points to an empty string, the function behaves as though no termination digits were supplied.

### -param dwFirstDigitTimeout

Time duration in milliseconds in which the first digit is expected. If the first digit is not received in this timeframe, digit collection is aborted and a 
<a href="/windows/desktop/Tapi/line-gatherdigits">LINE_GATHERDIGITS</a> message is sent to the application. The buffer only contains the <b>NULL</b> character, indicating that no digits were received and the first digit timeout terminated digit gathering. The call's line-device capabilities specify the valid range for this parameter or indicate that timeouts are not supported.

### -param dwInterDigitTimeout

Maximum time duration in milliseconds between consecutive digits. If no digit is received in this timeframe, digit collection is aborted and a LINE_GATHERDIGITS message is sent to the application. The buffer only contains the digits collected up to this point followed by a <b>NULL</b> character, indicating that an interdigit timeout terminated digit gathering. The call's line-device capabilities specify the valid range for this parameter or indicate that timeouts are not supported.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_NOMEM, LINEERR_INVALCALLSTATE, LINEERR_NOTOWNER, LINEERR_INVALDIGITMODE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALDIGITS, LINEERR_OPERATIONFAILED, LINEERR_INVALPARAM, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED.

## -remarks

Digit collection is terminated when the requested number of digits has been collected. It is also terminated when one of the digits detected matches a digit in <i>szTerminationDigits</i> before the specified number of digits has been collected. The detected termination digit is also placed in the buffer and the partial buffer is returned.

Another way of canceling digit collection occurs when one of the timeouts expires. The <i>dwFirstDigitTimeout</i> expires if the first digit is not received in this time period. The <i>dwInterDigitTimout</i> expires if the second, third, (and so forth) digit is not received within that time period from the previously detected digit, and a partial buffer is returned.

A fourth method for terminating digit collection is by calling this function again while collection is in progress. The old collection session is terminated, any digits collected up to that point are copied to the buffer supplied from the previous call to this function, and the buffer is delivered when the 
<a href="/windows/desktop/Tapi/line-gatherdigits">LINE_GATHERDIGITS</a> message is sent to the application. The mechanism for terminating digit gathering without initiating another gathering of the digits is to invoke this function with <i>lpsDigits</i> equal to <b>NULL</b>.

This function is considered successful if digit collection has been correctly initiated, not if digit collection has terminated. In all cases where a partial buffer is returned, valid digits (if any) are followed by a <b>NULL</b> character.

Although this function can be invoked in any call state, digits can typically only be gathered while the call is in the <i>connected</i> state.

The message LINE_GATHERDIGITS is sent only to the application that initiated the request. It is also sent when partial buffers are returned because of timeouts or matching termination digits, or when the request is canceled by another 
<b>lineGatherDigits</b> request on the call. Only one gather-digits request can be active on a call at any given time across all applications that are owners of the call. Given the asynchronous behavior of the operation, an application that issues multiple 
<b>lineGatherDigits</b> requests in quick succession may be able to do so and receive several LINE_GATHERDIGITS messages later. While this would be unusual application behavior, the application is able to count the number of these messages to allow cancel messages to be matched with the earlier requests. In any case, only the most recent request should be assumed to be valid.

<div class="alert"><b>Note</b>  When an application invokes any asynchronous operation that writes data back into application memory, the application must keep that memory available for writing until a 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> or 
<a href="/windows/desktop/Tapi/line-gatherdigits">LINE_GATHERDIGITS</a> message is received.</div>
<div> </div>
An application can use 
<a href="/windows/desktop/api/tapi/nf-tapi-linemonitordigits">lineMonitorDigits</a> to enable or disable unbuffered digit detection. Each time a digit is detected in this fashion, a 
<a href="/windows/desktop/Tapi/line-monitordigits">LINE_MONITORDIGITS</a> message is sent to the application. Both buffered and unbuffered digit detection can be simultaneously enabled for the same call.

Gathering of digits on a conference call applies only to the <i>hConfCall</i>, not to the individual participating calls.

If the 
<b>lineGatherDigits</b> function is used to cancel a previous request to gather digits, the function copies any digits collected up to that point to the buffer specified in the original function call. The function then sends a LINE_GATHERDIGITS message to the application, regardless of whether the <i>lpszDigits</i> parameter in the second call specifies a <b>NULL</b> or different address.





> [!NOTE]
> The tapi.h header defines lineGatherDigits as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/line-gatherdigits">LINE_GATHERDIGITS</a>



<a href="/windows/desktop/Tapi/line-monitordigits">LINE_MONITORDIGITS</a>



<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linemonitordigits">lineMonitorDigits</a>
