---
UID: NF:tspi.TSPI_lineAddToConference
title: TSPI_lineAddToConference function (tspi.h)
description: The TSPI_lineAddToConference function adds the call specified by hdConsultCall to the conference call specified by hdConfCall.
helpviewer_keywords: ["TSPI_lineAddToConference","TSPI_lineAddToConference function [TAPI 2.2]","_tspi_tspi_lineaddtoconference","tspi.tspi_lineaddtoconference","tspi/TSPI_lineAddToConference"]
old-location: tspi\tspi_lineaddtoconference.htm
tech.root: tapi3
ms.assetid: 6e3e3e1a-3a05-4464-9ead-abd647b3a721
ms.date: 12/05/2018
ms.keywords: TSPI_lineAddToConference, TSPI_lineAddToConference function [TAPI 2.2], _tspi_tspi_lineaddtoconference, tspi.tspi_lineaddtoconference, tspi/TSPI_lineAddToConference
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
 - TSPI_lineAddToConference
 - tspi/TSPI_lineAddToConference
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
 - TSPI_lineAddToConference
---

# TSPI_lineAddToConference function


## -description

The 
<b>TSPI_lineAddToConference</b> function adds the call specified by <i>hdConsultCall</i> to the conference call specified by <i>hdConfCall</i>.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdConfCall

The handle to the conference call. The call state of <i>hdConfCall</i> can be <i>onHoldPendingConference</i> or <i>onHold</i>.

### -param hdConsultCall

The handle to the call to be added to the conference call. This call cannot be either a parent of another conference or a participant in any conference. Depending on the device capabilities indicated in 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a>, the <i>hdConsultCall</i> parameter may not necessarily have been established using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetupconference">TSPI_lineSetupConference</a> or 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineprepareaddtoconference">TSPI_linePrepareAddToConference</a>. The call state of <i>hdConsultCall</i> can be <i>connected</i>, <i>onHold</i>, <i>proceeding</i>, or <i>ringback</i>.

## -returns

Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_CONFERENCEFULL, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM.

## -remarks

The service provider returns LINEERR_INVALCALLHANDLE if <i>hdConsultCall</i> is a parent of another conference or already a participant in a conference, or <i>hdConsultCall</i> cannot be added for other reasons, such as it must have been established using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetupconference">TSPI_lineSetupConference</a> or 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineprepareaddtoconference">TSPI_linePrepareAddToConference</a>.

<div class="alert"><b>Note</b>  The call handle of the added party remains valid after adding the call to a conference; typically, its state changes to <i>conferenced</i> while the state of the conference call becomes <i>connected</i>. The handle to an individual participating call can be used later to remove that party from the conference call using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineremovefromconference">TSPI_lineRemoveFromConference</a>.</div>
<div> </div>
The call states of the calls participating in a conference are not independent. For example, when dropping a conference call, all participating calls can automatically become <i>idle</i>. TAPI can consult the line's device capabilities to determine what form of conference removal is available. TAPI or its client applications should track the 
<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a> messages to determine what happened to the calls involved.

The conference call is established either through 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetupconference">TSPI_lineSetupConference</a> or 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linecompletetransfer">TSPI_lineCompleteTransfer</a>. Typically, the call added to a conference is established using 
<b>TSPI_lineSetupConference</b> or 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineprepareaddtoconference">TSPI_linePrepareAddToConference</a>. Some switches may allow adding of an arbitrary call to conference, and such a call may have been set up using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemakecall">TSPI_lineMakeCall</a> and be on (hard) hold. All calls that are part of a conference must exist on the same open line.

Any monitoring (media, tones, digits) on a conference call applies only to the <i>hdConfCall</i> parameter, not to the individual participating calls.

This function has no restrictions based on privilege as in the corresponding function at the TAPI level. There is no explicit requirement for the service provider to track the relationships between the "parent" conference call and its participants, because there is no TSPI correspondence to the TAPI function. Many service providers may find it necessary to track these relationships internally to implement the other conference call management functions.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linecompletetransfer">TSPI_lineCompleteTransfer</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineprepareaddtoconference">TSPI_linePrepareAddToConference</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineremovefromconference">TSPI_lineRemoveFromConference</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetupconference">TSPI_lineSetupConference</a>