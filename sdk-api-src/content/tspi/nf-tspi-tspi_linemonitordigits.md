---
UID: NF:tspi.TSPI_lineMonitorDigits
title: TSPI_lineMonitorDigits function
author: windows-sdk-content
description: The TSPI_lineMonitorDigits function enables and disables the unbuffered detection of digits received on the call.
old-location: tspi\tspi_linemonitordigits.htm
tech.root: Tapi
ms.assetid: 3153eb0e-32e9-40bf-b6aa-de594f6edbf6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TSPI_lineMonitorDigits, TSPI_lineMonitorDigits function [TAPI 2.2], _tspi_tspi_linemonitordigits, tspi.tspi_linemonitordigits, tspi/TSPI_lineMonitorDigits
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineMonitorDigits
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineMonitorDigits function


## -description


The 
<b>TSPI_lineMonitorDigits</b> function enables and disables the unbuffered detection of digits received on the call. Each time a digit of the specified digit mode(s) is detected, a 
<a href="https://msdn.microsoft.com/f1771e15-6356-4455-a951-ce0a2803bcfc">LINE_MONITORDIGITS</a> message is sent to the application by TAPI, indicating which digit is detected.


## -parameters




### -param hdCall

The handle to the call on which digits are to be detected. The call state of <i>hdCall</i> can be any state except <i>idle</i> or <i>disconnected</i>.


### -param dwDigitModes

The digit mode(s) that are to be monitored. A <i>dwDigitModes</i> parameter with a value of 0 cancels digit monitoring. The <i>dwDigitModes</i> parameter can have one of the 
<a href="https://msdn.microsoft.com/d603ea28-2b93-4548-bb16-78e93087f828">LINEDIGITMODE_ constants</a>.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALDIGITMODE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM.




## -remarks



This function returns zero (success) when digit monitoring is correctly initiated, not when digit monitoring is terminated. Digit monitoring remains in effect until it is explicitly disabled by a call to 
<b>TSPI_lineMonitorDigits</b> with <i>dwDigitModes</i> set to zero, or until the call transitions to <i>idle</i>. The function must return zero when digit monitoring is canceled (that is, when the <i>dwDigitModes</i> parameter is zero). The service provider must terminate digit monitoring when the call goes idle. TAPI does not spontaneously call 
<b>TSPI_lineMonitorDigits</b> to terminate monitoring.

Although this function can be invoked in any call state, digits typically are detected only while the call is in the <i>connected</i> state.

Each time a digit is detected, the service provider sends a 
<a href="https://msdn.microsoft.com/f1771e15-6356-4455-a951-ce0a2803bcfc">LINE_MONITORDIGITS</a> message to TAPI, passing the detected digit as a parameter. If both LINEDIGITMODE_DTMF and LINEDIGITMODE_DTMFEND are set in <i>dwDigitModes</i>, the two LINE_MONITORDIGITS messages are sent for each digit.

TAPI can use 
<b>TSPI_lineMonitorDigits</b> to enable or disable unbuffered digit detection. It can use 
<a href="https://msdn.microsoft.com/a7035e4d-dbb3-48b2-b44a-a7acb85e2d8a">TSPI_lineGatherDigits</a> for buffered digit detection. After buffered digit gathering is complete, a 
<a href="https://msdn.microsoft.com/bc625ff5-4af4-4e70-ab3a-1c12c74cff1c">LINE_GATHERDIGITS</a> message is sent. Both buffered and unbuffered digit detection can be enabled on the same call simultaneously.




## -see-also




<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/d603ea28-2b93-4548-bb16-78e93087f828">LINEDIGITMODE_ Constants</a>



<a href="https://msdn.microsoft.com/bc625ff5-4af4-4e70-ab3a-1c12c74cff1c">LINE_GATHERDIGITS</a>



<a href="https://msdn.microsoft.com/f1771e15-6356-4455-a951-ce0a2803bcfc">LINE_MONITORDIGITS</a>



<a href="https://msdn.microsoft.com/a7035e4d-dbb3-48b2-b44a-a7acb85e2d8a">TSPI_lineGatherDigits</a>



<a href="https://msdn.microsoft.com/6c5a668e-9a9a-4a7a-98e9-bd8ec4b819b2">TSPI_lineGetDevCaps</a>



<a href="https://msdn.microsoft.com/e9273bd6-8dc3-4b45-bf0e-a1a10d78a604">TSPI_lineSetMediaControl</a>
 

 

