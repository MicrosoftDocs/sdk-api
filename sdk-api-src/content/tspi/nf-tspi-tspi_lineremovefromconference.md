---
UID: NF:tspi.TSPI_lineRemoveFromConference
title: TSPI_lineRemoveFromConference function (tspi.h)
description: The TSPI_lineRemoveFromConference function removes the specified call from the conference call to which it currently belongs. The remaining calls in the conference call are unaffected.
helpviewer_keywords: ["TSPI_lineRemoveFromConference","TSPI_lineRemoveFromConference function [TAPI 2.2]","_tspi_tspi_lineremovefromconference","tspi.tspi_lineremovefromconference","tspi/TSPI_lineRemoveFromConference"]
old-location: tspi\tspi_lineremovefromconference.htm
tech.root: tapi3
ms.assetid: 6e09ba3e-d233-4026-9866-8bc0d45ec9aa
ms.date: 12/05/2018
ms.keywords: TSPI_lineRemoveFromConference, TSPI_lineRemoveFromConference function [TAPI 2.2], _tspi_tspi_lineremovefromconference, tspi.tspi_lineremovefromconference, tspi/TSPI_lineRemoveFromConference
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
 - TSPI_lineRemoveFromConference
 - tspi/TSPI_lineRemoveFromConference
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
 - TSPI_lineRemoveFromConference
---

# TSPI_lineRemoveFromConference function


## -description

The 
<b>TSPI_lineRemoveFromConference</b> function removes the specified call from the conference call to which it currently belongs. The remaining calls in the conference call are unaffected.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdCall

The handle to the call to be removed from the conference. The call state of <i>hdCall</i> can be <i>conferenced</i>.

## -returns

Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.

## -remarks

This operation removes a party that currently belongs to a conference call. After the call has been successfully removed, it may be possible to further manipulate it using its handle. The availability of this operation and its result are likely to be limited in many implementations. For example, in many implementations, only the most recently added party can be removed from a conference, and the removed call may be automatically dropped (becomes <i>idle</i>). The service provider indicates its capabilities in 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> with regard to the available effects of removing a call from a conference.

If the removal of a participant from a conference is supported, the service provider must indicate in the <b>dwRemoveFromConfState</b> member in 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a> the call state to which the call transitions after it is removed from the conference.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineaddtoconference">TSPI_lineAddToConference</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetdevcaps">TSPI_lineGetDevCaps</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetupconference">TSPI_lineSetupConference</a>