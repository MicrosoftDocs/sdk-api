---
UID: NF:tspi.TSPI_lineGetLineDevStatus
title: TSPI_lineGetLineDevStatus function (tspi.h)
description: The TSPI_lineGetLineDevStatus function queries the specified open line device for its current status. The information returned is global to all addresses on the line.
helpviewer_keywords: ["TSPI_lineGetLineDevStatus","TSPI_lineGetLineDevStatus function [TAPI 2.2]","_tspi_tspi_linegetlinedevstatus","tspi.tspi_linegetlinedevstatus","tspi/TSPI_lineGetLineDevStatus"]
old-location: tspi\tspi_linegetlinedevstatus.htm
tech.root: tapi3
ms.assetid: 14f7944b-e967-4967-9fb2-e7aeb78bb045
ms.date: 12/05/2018
ms.keywords: TSPI_lineGetLineDevStatus, TSPI_lineGetLineDevStatus function [TAPI 2.2], _tspi_tspi_linegetlinedevstatus, tspi.tspi_linegetlinedevstatus, tspi/TSPI_lineGetLineDevStatus
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
 - TSPI_lineGetLineDevStatus
 - tspi/TSPI_lineGetLineDevStatus
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
 - TSPI_lineGetLineDevStatus
---

# TSPI_lineGetLineDevStatus function


## -description

The 
<b>TSPI_lineGetLineDevStatus</b> function queries the specified open line device for its current status. The information returned is global to all addresses on the line.

## -parameters

### -param hdLine

The service provider's handle to the line to be queried.

### -param lpLineDevStatus

A pointer to a variably sized data structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a>. This structure is filled with the line's device status.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALLINEHANDLE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_OPERATIONUNAVAIL.

## -remarks

The following table indicates which members of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a> data structure are filled in by TAPI and which are filled in by the service provider. The service provider must preserve (it must not overwrite) the values filled in by TAPI.

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
<td><b>dwNumOpens;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>dwOpenMediaModes;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>dwNumActiveCalls;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwNumOnHoldCalls;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwNumOnHoldPendCalls;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwLineFeatures;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwNumCallCompletions;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwRingMode;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwSignalLevel;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwBatteryLevel;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwRoamMode;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwDevStatusFlags;</b></td>
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

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetaddressstatus">TSPI_lineGetAddressStatus</a>