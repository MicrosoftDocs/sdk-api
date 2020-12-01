---
UID: NF:tspi.TSPI_lineClose
title: TSPI_lineClose function (tspi.h)
description: The TSPI_lineClose function closes the specified open line device after completing or aborting all outstanding calls and asynchronous operations on the device.
helpviewer_keywords: ["TSPI_lineClose","TSPI_lineClose function [TAPI 2.2]","_tspi_tspi_lineclose","tspi.tspi_lineclose","tspi/TSPI_lineClose"]
old-location: tspi\tspi_lineclose.htm
tech.root: tapi3
ms.assetid: d1041620-609b-476b-bdb7-e1e0cebd74f1
ms.date: 12/05/2018
ms.keywords: TSPI_lineClose, TSPI_lineClose function [TAPI 2.2], _tspi_tspi_lineclose, tspi.tspi_lineclose, tspi/TSPI_lineClose
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
 - TSPI_lineClose
 - tspi/TSPI_lineClose
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
 - TSPI_lineClose
---

# TSPI_lineClose function


## -description

The 
<b>TSPI_lineClose</b> function closes the specified open line device after completing or aborting all outstanding calls and asynchronous operations on the device.

## -parameters

### -param hdLine

The service provider's handle to the line to be closed. After the line is successfully closed, this handle is no longer valid.

## -returns

Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL.

## -remarks

The service provider must report completion for every asynchronous operation. If 
<b>TSPI_lineClose</b> is called for a line on which there are outstanding asynchronous operations, the operations are reported complete with an appropriate result or error code before this procedure returns.

A similar requirement exists for active calls on the line. Outstanding operations must be reported complete with appropriate result or error codes. Active calls must also be dropped, if required, and if this behavior was indicated by the LINEDEVCAPFLAGS_CLOSEDROP bit in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure.

After this procedure returns, the service provider must report no further <i>htCall</i> on the line or calls that were on the line. The service provider's handles for the line and calls on the line become "invalid."

The service provider must relinquish nonsharable resources it reserves while the line is open. For example, closing a line accessed through a comm port and modem should result in closing the comm port, making it once again available for use by other applications.

The service provider does not issue the 
<a href="/previous-versions/windows/desktop/legacy/ms725231(v=vs.85)">LINE_LINEDEVSTATE</a> message in response to this function invocation because the line closes and there is no longer any interest in its state changes.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/previous-versions/windows/desktop/legacy/ms725220(v=vs.85)">LINE_CLOSE</a>



<a href="/previous-versions/windows/desktop/legacy/ms725231(v=vs.85)">LINE_LINEDEVSTATE</a>