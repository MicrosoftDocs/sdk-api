---
UID: NF:tspi.TSPI_lineCloseCall
title: TSPI_lineCloseCall function (tspi.h)
description: The TSPI_lineCloseCall function deallocates the call after completing or aborting all outstanding asynchronous operations on the call.
helpviewer_keywords: ["TSPI_lineCloseCall","TSPI_lineCloseCall function [TAPI 2.2]","_tspi_tspi_lineclosecall","tspi.tspi_lineclosecall","tspi/TSPI_lineCloseCall"]
old-location: tspi\tspi_lineclosecall.htm
tech.root: tapi3
ms.assetid: 86f5490c-8401-4235-8ddd-313794bd5bf1
ms.date: 12/05/2018
ms.keywords: TSPI_lineCloseCall, TSPI_lineCloseCall function [TAPI 2.2], _tspi_tspi_lineclosecall, tspi.tspi_lineclosecall, tspi/TSPI_lineCloseCall
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
 - TSPI_lineCloseCall
 - tspi/TSPI_lineCloseCall
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
 - TSPI_lineCloseCall
---

# TSPI_lineCloseCall function


## -description

The 
<b>TSPI_lineCloseCall</b> function deallocates the call after completing or aborting all outstanding asynchronous operations on the call.

## -parameters

### -param hdCall

The service provider's handle to the call to be closed. After the call is successfully closed, this handle is no longer valid. The call state can be any state.

## -returns

Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL.

## -remarks

The service provider must report completion for asynchronous operations. If 
<b>TSPI_lineCloseCall</b> is called for a call on which there are outstanding asynchronous operations, the operations should be reported complete with an appropriate result or error code before this procedure returns. After this procedure returns, the service provider must report no further events on the call. The service provider's handles for the line and calls on the line become "invalid."

TAPI does not call 
<b>TSPI_lineCloseCall</b> if a service provider synchronously returns an error from a call to the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemakecall">TSPI_lineMakeCall</a> function. But TAPI does call 
<b>TSPI_lineCloseCall</b> if the service provider returns an error from the asynchronous operation initiated by 
<b>TSPI_lineMakeCall</b>.

If there is an active call on the line at the time of 
<b>TSPI_lineCloseCall</b>, the call must be dropped if this behavior is indicated by the LINEDEVCAPFLAGS_CLOSEDROP bit in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure.

If the service provider can determine that there is another agent sharing control of the call, such as in a party line situation with a separate handset, the service provider simply lets control of the call pass to the other agent rather than forcibly dropping it.

This function should always succeed except in extraordinary circumstances. Most callers will probably ignore the return code because they will be unable to compensate for any error that occurs. The specified return values are more advisory for development diagnostic purposes than anything else.

This function is called when the last application with a handle to this call executes 
<a href="/windows/desktop/api/tapi/nf-tapi-linedeallocatecall">lineDeallocateCall</a>.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemakecall">TSPI_lineMakeCall</a>