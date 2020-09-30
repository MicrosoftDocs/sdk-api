---
UID: NF:tspi.TSPI_lineSecureCall
title: TSPI_lineSecureCall function (tspi.h)
description: The TSPI_lineSecureCall function secures the call from any interruptions or interference that can affect the call's media stream.
helpviewer_keywords: ["TSPI_lineSecureCall","TSPI_lineSecureCall function [TAPI 2.2]","_tspi_tspi_linesecurecall","tspi.tspi_linesecurecall","tspi/TSPI_lineSecureCall"]
old-location: tspi\tspi_linesecurecall.htm
tech.root: tapi3
ms.assetid: a064bf4b-3401-4f92-b318-a9f66de1e61f
ms.date: 12/05/2018
ms.keywords: TSPI_lineSecureCall, TSPI_lineSecureCall function [TAPI 2.2], _tspi_tspi_linesecurecall, tspi.tspi_linesecurecall, tspi/TSPI_lineSecureCall
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
 - TSPI_lineSecureCall
 - tspi/TSPI_lineSecureCall
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
 - TSPI_lineSecureCall
---

# TSPI_lineSecureCall function


## -description

The 
<b>TSPI_lineSecureCall</b> function secures the call from any interruptions or interference that can affect the call's media stream.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdCall

The handle to the call to be secured. The call state of <i>hdCall</i> can be any state except <i>idle</i>.

## -returns

Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.

## -remarks

A call can be secured to avoid interference. For example, in an analog environment, call waiting tones can destroy a fax or modem session on the original call. 
<b>TSPI_lineSecureCall</b> allows an existing call to be secured, 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemakecall">TSPI_lineMakeCall</a> provides the option to secure the call from the time of call setup. The securing of a call remains in effect for the duration of the call.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemakecall">TSPI_lineMakeCall</a>