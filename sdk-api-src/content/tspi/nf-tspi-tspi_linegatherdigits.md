---
UID: NF:tspi.TSPI_lineGatherDigits
title: TSPI_lineGatherDigits function (tspi.h)
description: The TSPI_lineGatherDigits function initiates the buffered gathering of digits on the specified call. TAPI specifies a buffer in which to place the digits and the maximum number of digits to be collected.
helpviewer_keywords: ["LINEDIGITMODE_DTMF","LINEDIGITMODE_PULSE","TSPI_lineGatherDigits","TSPI_lineGatherDigits function [TAPI 2.2]","_tspi_tspi_linegatherdigits","tspi.tspi_linegatherdigits","tspi/TSPI_lineGatherDigits"]
old-location: tspi\tspi_linegatherdigits.htm
tech.root: tapi3
ms.assetid: a7035e4d-dbb3-48b2-b44a-a7acb85e2d8a
ms.date: 12/05/2018
ms.keywords: LINEDIGITMODE_DTMF, LINEDIGITMODE_PULSE, TSPI_lineGatherDigits, TSPI_lineGatherDigits function [TAPI 2.2], _tspi_tspi_linegatherdigits, tspi.tspi_linegatherdigits, tspi/TSPI_lineGatherDigits
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
 - TSPI_lineGatherDigits
 - tspi/TSPI_lineGatherDigits
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
 - TSPI_lineGatherDigits
---

# TSPI_lineGatherDigits function


## -description

The 
<b>TSPI_lineGatherDigits</b> function initiates the buffered gathering of digits on the specified call. TAPI specifies a buffer in which to place the digits and the maximum number of digits to be collected.

## -parameters

### -param hdCall

The service provider's handle to the call on which digit gathering is to be performed. The call state of <i>hdCall</i> can be any state except <i>idle</i>.

### -param dwEndToEndID

A unique, uninterpreted identifier of the request for its entire lifetime, that is, until the matching 
<a href="/previous-versions/windows/desktop/legacy/ms725229(v=vs.85)">LINE_GATHERDIGITS</a> message is sent. The service provider includes this identifier as one of the parameters in the message.

### -param dwDigitModes

The digit mode(s) that are to be monitored. This parameter uses one or more of the following LINEDIGITMODE_ constants.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LINEDIGITMODE_PULSE"></a><a id="linedigitmode_pulse"></a><dl>
<dt><b>LINEDIGITMODE_PULSE</b></dt>
</dl>
</td>
<td width="60%">
Detect digits as audible clicks that are the result of the use of rotary pulse sequences. Valid digits for pulse mode are '0' through '9'.

</td>
</tr>
<tr>
<td width="40%"><a id="LINEDIGITMODE_DTMF"></a><a id="linedigitmode_dtmf"></a><dl>
<dt><b>LINEDIGITMODE_DTMF</b></dt>
</dl>
</td>
<td width="60%">
Detect digits as DTMF tones. Valid digits for DTMF mode are '0' through '9', 'A', 'B', 'C', 'D', '*', '#'.

</td>
</tr>
</table>

### -param lpsDigits

A pointer to the buffer where detected digits are to be stored as text characters. The service provider may, but is not required to, place digits in the buffer one at a time as they are collected. When the 
<a href="/previous-versions/windows/desktop/legacy/ms725229(v=vs.85)">LINE_GATHERDIGITS</a> message is sent, the content of the buffer must be complete. If <i>lpsDigits</i> is specified as <b>NULL</b> the digit gathering currently in progress on the call is canceled and the <i>dwNumDigits</i> parameter is ignored. Otherwise, <i>lpsDigits</i> is assumed to have room for <i>dwNumDigits</i> digits.

### -param dwNumDigits

The number of digits to be collected before a LINE_GATHERDIGITS message is sent to TAPI. The <i>dwNumDigits</i> parameter is ignored when <i>lpsDigits</i> is <b>NULL</b>. This function must return a LINEERR_INVALPARAM if <i>dwNumDigits</i> is zero.

### -param lpszTerminationDigits

Pointer to a <b>null</b>-terminated Unicode string of termination digits as text characters. If one of the digits in the string is detected, that termination digit is appended to the buffer, digit collection is terminated, and the 
<a href="/previous-versions/windows/desktop/legacy/ms725229(v=vs.85)">LINE_GATHERDIGITS</a> message is sent to TAPI. 




Valid characters for pulse mode are '0' through '9'. Valid characters for DTMF mode are '0' through '9', 'A', 'B', 'C', 'D', '*', '#'. If this pointer is <b>NULL</b>, or if it points to an empty string, the function behaves as though no termination digits were supplied.

### -param dwFirstDigitTimeout

The time duration in milliseconds in which the first digit is expected. If the first digit is not received in this timeframe, digit collection is terminated and a LINE_GATHERDIGITS message is sent to TAPI. A single <b>NULL</b> character is written to the buffer, indicating no digits were received and the first digit timeout terminated digit gathering. The call's line device capabilities specifies the valid range for this parameter or indicates that timeouts are not supported. This parameter is not validated by TAPI when this function is called.

### -param dwInterDigitTimeout

The maximum time duration in milliseconds between consecutive digits. If no digit is received in this timeframe, digit collection is terminated and a 
<a href="/previous-versions/windows/desktop/legacy/ms725229(v=vs.85)">LINE_GATHERDIGITS</a> message is sent to TAPI. A single NULL character is written to the buffer, indicating that an interdigit timeout terminated digit gathering. The 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure must specify the valid range for this parameter or indicate that timeouts are not supported. This parameter is not validated by TAPI when this function is called.

## -returns

Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_NOMEM, LINEERR_INVALTIMEOUT, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALDIGITMODE, LINEERR_OPERATIONFAILED, LINEERR_INVALDIGITS, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPARAM.

## -remarks

The service provider returns LINEERR_INVALPARAM if the <i>dwNumDigits</i> parameter is invalid.

This function returns zero (success) if digit collection is correctly initiated; not if digit collection has terminated. In all cases where a partial buffer is returned, valid digits (if any) are followed by an Unicode NULL character.

Digit collection can be terminated in the following ways:

<ul>
<li>The requested number of digits may have been collected.</li>
<li>One of the digits detected matches a digit in <i>szTerminationDigits</i> before the specified number of digits has been collected. The detected termination digit is also placed in the buffer and the partial buffer is returned.</li>
<li>One of the timeouts expires. The <i>dwFirstDigitTimeout</i> expires if the first digit is not received in this time period. The <i>dwInterDigitTimout</i> expires if the second, third, (and so forth) digit is not received within that time period from the previously detected digit, and a partial buffer is returned.</li>
<li>Calling this operation again while collection is in progress. The old collection session is terminated and the contents of the old buffer is undefined. To cancel digit gathering without initiating another operation, this operation is invoked with <i>lpsDigits</i> equal to NULL.</li>
</ul>
Although this function can be invoked in any call state except <i>idle</i>, digits can typically only be gathered while the call is in the <i>connected</i> state.

The 
<a href="/previous-versions/windows/desktop/legacy/ms725229(v=vs.85)">LINE_GATHERDIGITS</a> message is normally sent when the digit buffer becomes filled. It is also sent when partial buffers are returned because of timeouts or matching termination digits, or when the request is canceled through another 
<b>TSPI_lineGatherDigits</b> request on the call. Only one gather digits request can be active at a time. The service provider must terminate any outstanding gathering operation with a LINE_GATHERDIGITS message when 
<b>TSPI_lineGatherDigits</b> is called.

When the operation associated with a call to the 
<b>TSPI_lineGatherDigits</b> function is canceled (by a subsequent call to the function), the service provider copies any digits collected up to that point to the buffer specified in the original call.

TAPI can use 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemonitordigits">TSPI_lineMonitorDigits</a> to enable or disable unbuffered digit detection. Each time a digit is detected in this fashion, a 
<a href="/previous-versions/windows/desktop/legacy/ms725232(v=vs.85)">LINE_MONITORDIGITS</a> message is sent to TAPI. Both buffered (gather digits) and unbuffered digit detection can be enabled for the same call simultaneously.

The service provider is allowed some variation in the quality of timing it uses for this function, including not doing timings at all. The quality of timing is reported in 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>, in the members <b>dwGatherDigitsMinTimeout</b> and <b>dwGatherDigitsMaxTimeout</b>.

The corresponding function at the TAPI level does not include the formal parameter <i>dwEndToEndID</i>. At that level, there is no end-to-end marking. TAPI uses end-to-end marking at the TSPI level to distinguish one 
<b>TSPI_lineGatherDigits</b> request from another.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/Tapi/linedigitmode--constants">LINEDIGITMODE_ Constants</a>



<a href="/previous-versions/windows/desktop/legacy/ms725229(v=vs.85)">LINE_GATHERDIGITS</a>



<a href="/previous-versions/windows/desktop/legacy/ms725232(v=vs.85)">LINE_MONITORDIGITS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetdevcaps">TSPI_lineGetDevCaps</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemonitordigits">TSPI_lineMonitorDigits</a>