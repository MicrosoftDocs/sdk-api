---
UID: NF:tspi.TSPI_lineMonitorDigits
title: TSPI_lineMonitorDigits function (tspi.h)
description: The TSPI_lineMonitorDigits function enables and disables the unbuffered detection of digits received on the call.
helpviewer_keywords: ["TSPI_lineMonitorDigits","TSPI_lineMonitorDigits function [TAPI 2.2]","_tspi_tspi_linemonitordigits","tspi.tspi_linemonitordigits","tspi/TSPI_lineMonitorDigits"]
old-location: tspi\tspi_linemonitordigits.htm
tech.root: tapi3
ms.assetid: 3153eb0e-32e9-40bf-b6aa-de594f6edbf6
ms.date: 12/05/2018
ms.keywords: TSPI_lineMonitorDigits, TSPI_lineMonitorDigits function [TAPI 2.2], _tspi_tspi_linemonitordigits, tspi.tspi_linemonitordigits, tspi/TSPI_lineMonitorDigits
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
 - TSPI_lineMonitorDigits
 - tspi/TSPI_lineMonitorDigits
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
 - TSPI_lineMonitorDigits
---

# TSPI_lineMonitorDigits function


## -description

The 
<b>TSPI_lineMonitorDigits</b> function enables and disables the unbuffered detection of digits received on the call. Each time a digit of the specified digit mode(s) is detected, a 
<a href="/previous-versions/windows/desktop/legacy/ms725232(v=vs.85)">LINE_MONITORDIGITS</a> message is sent to the application by TAPI, indicating which digit is detected.

## -parameters

### -param hdCall

The handle to the call on which digits are to be detected. The call state of <i>hdCall</i> can be any state except <i>idle</i> or <i>disconnected</i>.

### -param dwDigitModes

The digit mode(s) that are to be monitored. A <i>dwDigitModes</i> parameter with a value of 0 cancels digit monitoring. The <i>dwDigitModes</i> parameter can have one of the 
<a href="/windows/desktop/Tapi/linedigitmode--constants">LINEDIGITMODE_ constants</a>.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALDIGITMODE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM.

## -remarks

This function returns zero (success) when digit monitoring is correctly initiated, not when digit monitoring is terminated. Digit monitoring remains in effect until it is explicitly disabled by a call to 
<b>TSPI_lineMonitorDigits</b> with <i>dwDigitModes</i> set to zero, or until the call transitions to <i>idle</i>. The function must return zero when digit monitoring is canceled (that is, when the <i>dwDigitModes</i> parameter is zero). The service provider must terminate digit monitoring when the call goes idle. TAPI does not spontaneously call 
<b>TSPI_lineMonitorDigits</b> to terminate monitoring.

Although this function can be invoked in any call state, digits typically are detected only while the call is in the <i>connected</i> state.

Each time a digit is detected, the service provider sends a 
<a href="/previous-versions/windows/desktop/legacy/ms725232(v=vs.85)">LINE_MONITORDIGITS</a> message to TAPI, passing the detected digit as a parameter. If both LINEDIGITMODE_DTMF and LINEDIGITMODE_DTMFEND are set in <i>dwDigitModes</i>, the two LINE_MONITORDIGITS messages are sent for each digit.

TAPI can use 
<b>TSPI_lineMonitorDigits</b> to enable or disable unbuffered digit detection. It can use 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegatherdigits">TSPI_lineGatherDigits</a> for buffered digit detection. After buffered digit gathering is complete, a 
<a href="/previous-versions/windows/desktop/legacy/ms725229(v=vs.85)">LINE_GATHERDIGITS</a> message is sent. Both buffered and unbuffered digit detection can be enabled on the same call simultaneously.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/Tapi/linedigitmode--constants">LINEDIGITMODE_ Constants</a>



<a href="/previous-versions/windows/desktop/legacy/ms725229(v=vs.85)">LINE_GATHERDIGITS</a>



<a href="/previous-versions/windows/desktop/legacy/ms725232(v=vs.85)">LINE_MONITORDIGITS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegatherdigits">TSPI_lineGatherDigits</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetdevcaps">TSPI_lineGetDevCaps</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetmediacontrol">TSPI_lineSetMediaControl</a>