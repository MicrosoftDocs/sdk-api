---
UID: NF:tspi.TSPI_linePark
title: TSPI_linePark function (tspi.h)
description: The TSPI_linePark function parks the specified call according to the specified park mode.
helpviewer_keywords: ["TSPI_linePark","TSPI_linePark function [TAPI 2.2]","_tspi_tspi_linepark","tspi.tspi_linepark","tspi/TSPI_linePark"]
old-location: tspi\tspi_linepark.htm
tech.root: tapi3
ms.assetid: 6ff14bfc-ba48-4f70-b732-81c19dba92c5
ms.date: 12/05/2018
ms.keywords: TSPI_linePark, TSPI_linePark function [TAPI 2.2], _tspi_tspi_linepark, tspi.tspi_linepark, tspi/TSPI_linePark
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
 - TSPI_linePark
 - tspi/TSPI_linePark
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
 - TSPI_linePark
---

# TSPI_linePark function


## -description

The 
<b>TSPI_linePark</b> function parks the specified call according to the specified park mode.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdCall

The handle to the call to be parked. The call state of <i>hdCall</i> can be <i>connected</i>.

### -param dwParkMode

The park mode with which the call is to be parked, only one of the 
<a href="/windows/desktop/Tapi/lineparkmode--constants">LINEPARKMODE_ constants</a>.

### -param lpszDirAddress

A pointer to <b>null</b>-terminated Unicode string that indicates the address where the call is to be parked when using directed park. The address is in dialable address format. This parameter is ignored for nondirected park.

### -param lpNonDirAddress

A pointer to a structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a>. For nondirected park, the address where the call is parked is returned in this structure. This parameter is ignored for directed park. Within the 
<b>VARSTRING</b> structure, <i>dwStringFormat</i> must be set to STRINGFORMAT_ASCII (an ASCII string buffer containing a <b>null</b>-terminated string), and the terminating <b>NULL</b> is accounted for in the <i>dwStringSize</i>. If the memory pointed to by the <i>lpNonDirAddress</i> parameter is not large enough for the requested address, the 
<b>TSPI_linePark</b> function returns LINEERR_STRUCTURETOOSMALL.

## -returns

Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_NOMEM, LINEERR_INVALPARKMODE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALADDRESS, LINEERR_RESOURCEUNAVAIL, LINEERR_STRUCTURETOOSMALL.

## -remarks

All members of the 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> structure, except <b>dwTotalSize</b>, are filled in by the service provider. The <b>dwTotalSize</b> member is filled in by TAPI, and the service provider must not overwrite this value.

Under directed park, the client application (through TAPI) specifies the address at which it wants to park the call. Under nondirected park, the switch determines the address and provides this to TAPI. In either case, a parked call can be unparked by specifying this address.

The parked call typically enters the <i>idle</i> call state after it is successfully parked. The service provider reports the new state using a 
<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a> message. A subsequent 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineunpark">TSPI_lineUnpark</a> creates a new, distinct call handle, regardless of whether 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineclosecall">TSPI_lineCloseCall</a> has destroyed the old handle.

Some switches can remind the user after a call has been parked for some long amount of time. The service provider reports this to TAPI as an <i>offering</i> call with a call reason set to <i>reminder</i> (if this is known).

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/Tapi/lineparkmode--constants">LINEPARKMODE_ Constants</a>



<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineclosecall">TSPI_lineCloseCall</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineunpark">TSPI_lineUnpark</a>



<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a>