---
UID: NF:tspi.TSPI_lineSetCallParams
title: TSPI_lineSetCallParams function (tspi.h)
description: The TSPI_lineSetCallParams function sets certain parameters for an existing call.
helpviewer_keywords: ["TSPI_lineSetCallParams","TSPI_lineSetCallParams function [TAPI 2.2]","_tspi_tspi_linesetcallparams","tspi.tspi_linesetcallparams","tspi/TSPI_lineSetCallParams"]
old-location: tspi\tspi_linesetcallparams.htm
tech.root: tapi3
ms.assetid: cc5d5347-ebb7-437a-a9a1-311b6c2a78ab
ms.date: 12/05/2018
ms.keywords: TSPI_lineSetCallParams, TSPI_lineSetCallParams function [TAPI 2.2], _tspi_tspi_linesetcallparams, tspi.tspi_linesetcallparams, tspi/TSPI_lineSetCallParams
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
 - TSPI_lineSetCallParams
 - tspi/TSPI_lineSetCallParams
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
 - TSPI_lineSetCallParams
---

# TSPI_lineSetCallParams function


## -description

The 
<b>TSPI_lineSetCallParams</b> function sets certain parameters for an existing call.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdCall

The handle to the call whose parameters are to be changed. The call state can be any state except <i>idle</i> and <i>disconnected</i>.

### -param dwBearerMode

The new bearer mode for the call. The <i>dwBearerMode</i> parameter can have only one of the 
<a href="/windows/desktop/Tapi/linebearermode--constants">LINEBEARERMODE_ constants</a>.

### -param dwMinRate

A lower bound for the call's new data rate. TAPI can accept a new rate as low as this one. TAPI does not validate this parameter when this function is called.

### -param dwMaxRate

An upper bound for the call's new data rate. This is the maximum data rate TAPI would like. Equal values for <i>dwMinRate</i> and <i>dwMaxRate</i> indicate that an exact data rate is required. TAPI does not validate this parameter when this function is called.

### -param lpDialParams

A pointer to the new dial parameters for the call, of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linedialparams">LINEDIALPARAMS</a>. If this parameter is <b>NULL</b>, it indicates that the call's current dialing parameters are to be used.

## -returns

Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_RATEUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_NOMEM, LINEERR_INVALBEARERMODE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALPOINTER, LINEERR_OPERATIONFAILED, LINEERR_INVALRATE, LINEERR_RESOURCEUNAVAIL, LINEERR_BEARERMODEUNAVAIL.

## -remarks

This operation is used to change the parameters of an existing call. Examples of its usage include changing the bearer mode and/or the data rate of an existing call.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedialparams">LINEDIALPARAMS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemakecall">TSPI_lineMakeCall</a>