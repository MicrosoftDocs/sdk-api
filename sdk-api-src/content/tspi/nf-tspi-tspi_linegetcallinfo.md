---
UID: NF:tspi.TSPI_lineGetCallInfo
title: TSPI_lineGetCallInfo function (tspi.h)
description: The TSPI_lineGetCallInfo function returns detailed information about the specified call.
helpviewer_keywords: ["TSPI_lineGetCallInfo","TSPI_lineGetCallInfo function [TAPI 2.2]","_tspi_tspi_linegetcallinfo","tspi.tspi_linegetcallinfo","tspi/TSPI_lineGetCallInfo"]
old-location: tspi\tspi_linegetcallinfo.htm
tech.root: tapi3
ms.assetid: 9ef43928-05aa-4ec6-bc44-f07a63d8ecdf
ms.date: 12/05/2018
ms.keywords: TSPI_lineGetCallInfo, TSPI_lineGetCallInfo function [TAPI 2.2], _tspi_tspi_linegetcallinfo, tspi.tspi_linegetcallinfo, tspi/TSPI_lineGetCallInfo
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
 - TSPI_lineGetCallInfo
 - tspi/TSPI_lineGetCallInfo
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
 - TSPI_lineGetCallInfo
---

# TSPI_lineGetCallInfo function


## -description

The 
<b>TSPI_lineGetCallInfo</b> function returns detailed information about the specified call.

## -parameters

### -param hdCall

The service provider's handle to the call whose call information is to be retrieved. The call state of <i>hdCall</i> can be any state.

### -param lpCallInfo

A pointer to a variably sized data structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>. Upon successful completion of the request, this structure is filled with call-related information.

## -returns

Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_OPERATIONUNAVAIL.

## -remarks

The following table indicates which members of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> data structure are filled in by TAPI and which members are filled in by the service provider. The service provider must preserve (it must not overwrite) the values filled in by TAPI.

<table>
<tr>
<th>Member name</th>
<th>TAPI</th>
<th>Service provider</th>
</tr>
<tr>
<td><b>dwTotalSize;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>dwNeededSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwUsedSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>hLine;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>dwLineDeviceID;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwAddressID;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwBearerMode;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwRate;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwMediaMode;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwAppSpecific;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwCallID;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwRelatedCallID;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwCallParamFlags;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwCallStates;</b></td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td><b>dwMonitorDigitModes;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>dwMonitorMediaModes;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>DialParams;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwOrigin;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwReason;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwCompletionID;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwNumOwners;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>dwNumMonitors;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>dwCountryCode;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwTrunk;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwCallerIDFlags;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwCallerIDSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwCallerIDOffset;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwCallerIDNameSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwCallerIDNameOffset;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwCalledIDFlags;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwCalledIDSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwCalledIDOffset;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwCalledIDNameSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwCalledIDNameOffset;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwConnectedIDFlags;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwConnectedIDSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwConnectedIDOffset;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwConnectedIDNameSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwConnectedIDNameOffset;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwRedirectionIDFlags;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwRedirectionIDSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwRedirectionIDOffset;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwRedirectionIDNameSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwRedirectionIDNameOffset;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwRedirectingIDFlags;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwRedirectingIDSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwRedirectingIDOffset;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwRedirectingIDNameSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwRedirectingIDNameOffset;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwAppNameSize;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>dwAppNameOffset;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>dwDisplayableAddressSize;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>dwDisplayableAddressOffset;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>dwCalledPartySize;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>dwCalledPartyOffset;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>dwCommentSize;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>dwCommentOffset;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>dwDisplaySize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwDisplayOffset;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwUserUserInfoSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwUserUserInfoOffset;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwHighLevelCompSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwHighLevelCompOffset;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwLowLevelCompSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwLowLevelCompOffset;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwChargingInfoSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwChargingInfoOffset;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwTerminalModesSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwTerminalModesOffset;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwDevSpecificSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwDevSpecificOffset;</b></td>
<td></td>
<td>X</td>
</tr>
</table>
 

TAPI fills in the size and offset fields for the <b>dwAppNameSize/Offset</b>, <b>dwCalledPartySize/Offset</b>, and <b>dwCommentSize/Offset</b> members and updates the value in <b>dwUsedSize</b> to reflect these after calling the service provider.

After the service provider returns from the 
<b>TSPI_lineGetCallInfo</b> function, TAPI sets the <b>dwCallStates</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure as follows:


``` syntax
LINECALLINFO.dwCallStates |= LINECALLSTATE_UNKNOWN;
```

If the service provider models lines as "pools" of channel resources and does inverse multiplexing of a call over several address identifiers, it should consistently choose one of these address identifiers as the primary identifier reported by this function in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> data structure.
