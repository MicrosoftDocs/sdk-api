---
UID: NF:tapi.lineAddToConference
title: lineAddToConference function (tapi.h)
description: The lineAddToConference function adds the call specified by hConsultCall to the conference call specified by hConfCall.
helpviewer_keywords: ["_tapi2_lineaddtoconference","lineAddToConference","lineAddToConference function [TAPI 2.2]","tapi/lineAddToConference","tapi2.lineaddtoconference"]
old-location: tapi2\lineaddtoconference.htm
tech.root: tapi3
ms.assetid: fbbaea96-727c-46b9-91d1-31d3f89d8ad8
ms.date: 12/05/2018
ms.keywords: _tapi2_lineaddtoconference, lineAddToConference, lineAddToConference function [TAPI 2.2], tapi/lineAddToConference, tapi2.lineaddtoconference
req.header: tapi.h
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineAddToConference
 - tapi/lineAddToConference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineAddToConference
---

# lineAddToConference function


## -description

The 
<b>lineAddToConference</b> function adds the call specified by <i>hConsultCall</i> to the conference call specified by <i>hConfCall</i>.

## -parameters

### -param hConfCall

Handle to the conference call. The application must be an owner of this call. Any monitoring (media, tones, digits) on a conference call applies only to the <i>hConfCall</i>, not to the individual participating calls. Call state of <i>hConfCall</i> must be <i>onHoldPendingConference</i> or <i>onHold</i>.

### -param hConsultCall

Handle to the call to be added to the conference call. The application must be an owner of this call. This call cannot be a parent of another conference or a participant in any conference. Depending on the device capabilities indicated in 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a>, the <i>hConsultCall</i> may not necessarily have been established using 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetupconference">lineSetupConference</a> or 
<a href="/windows/desktop/api/tapi/nf-tapi-lineprepareaddtoconference">linePrepareAddToConference</a>. The call state of <i>hConsultCall</i> must be <i>connected</i>, <i>onHold</i>, <i>proceeding</i>, or <i>ringback</i>. Many PBXs allow calls to be added to conferences before they are actually answered.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds, or it is a negative error number if an error occurs. Possible return values are:

LINEERR_CONFERENCEFULL, LINEERR_NOTOWNER, LINEERR_INVALCONFCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSTATE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.

## -remarks

If LINEERR_INVALCALLHANDLE is returned, the specified call handle for the added call is invalid; <i>hConsultCall</i> is a parent of another conference or already a participant in a conference; <i>hConsultCall</i> cannot be added for other reasons (such as, it must have been established using 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetupconference">lineSetupConference</a> or 
<a href="/windows/desktop/api/tapi/nf-tapi-lineprepareaddtoconference">linePrepareAddToConference</a>); or <i>hConsultCall</i> and <i>hConfCall</i> are calls on different open lines.

The call handle of the added party remains valid after adding the call to a conference. Its state typically changes to <i>conferenced</i> while the state of the conference call typically becomes <i>connected</i>. Using 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetconfrelatedcalls">lineGetConfRelatedCalls</a>, you can obtain a list of call handles that are part of the same conference call as the specified call. The specified call is either a conference call or a participant call in a conference call. New handles are generated for those calls for which the application does not already have handles, and the application is granted monitor privilege to those calls. The handle to an individual participating call can be used later to remove that party from the conference call using 
<a href="/windows/desktop/api/tapi/nf-tapi-lineremovefromconference">lineRemoveFromConference</a>.

If 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetconfrelatedcalls">lineGetConfRelatedCalls</a> is called immediately after 
<b>lineAddToConference</b>, it may not return a complete list of related calls because TAPI waits to receive a 
<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a> message indicating that the call has entered LINECALLSTATE_CONFERENCED before it considers the call to actually be part of the conference (that is, the conferenced state is confirmed by the service provider). After the application has received the LINE_CALLSTATE message, 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetconfrelatedcalls">lineGetConfRelatedCalls</a> returns complete information.

<div class="alert"><b>Note</b>  All calls that are part of a conference must exist on the same open line.</div>
<div> </div>
The call states of the calls participating in a conference are not independent. For example, when dropping a conference call, all participating calls can automatically become idle. An application should consult the line's device capabilities to determine what form of conference removal is available. The application should track the LINE_CALLSTATE messages to determine what happened to the calls involved.

The conference call is established either by 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetupconference">lineSetupConference</a> or 
<a href="/windows/desktop/api/tapi/nf-tapi-linecompletetransfer">lineCompleteTransfer</a>. The call added to a conference is typically established using 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetupconference">lineSetupConference</a> or 
<a href="/windows/desktop/api/tapi/nf-tapi-lineprepareaddtoconference">linePrepareAddToConference</a>. Some switches can allow adding arbitrary calls to the conference, and such a call can have been set up using 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a> and be on (hard) hold. The application can examine the <b>dwAddrCapFlags</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a> structure to determine the permitted operations.

## -see-also

<a href="/windows/desktop/Tapi/conference-ovr">Conference overview</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a>



<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linecompletetransfer">lineCompleteTransfer</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetconfrelatedcalls">lineGetConfRelatedCalls</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineprepareaddtoconference">linePrepareAddToConference</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineremovefromconference">lineRemoveFromConference</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetupconference">lineSetupConference</a>