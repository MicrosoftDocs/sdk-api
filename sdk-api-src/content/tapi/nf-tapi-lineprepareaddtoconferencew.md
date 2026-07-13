---
UID: NF:tapi.linePrepareAddToConferenceW
title: linePrepareAddToConferenceW function (tapi.h)
description: The linePrepareAddToConferenceW (Unicode) function (tapi.h) prepares an existing conference call for the addition of another party. 
helpviewer_keywords: ["_tapi2_lineprepareaddtoconference", "linePrepareAddToConference", "linePrepareAddToConference function [TAPI 2.2]", "linePrepareAddToConferenceW", "tapi/linePrepareAddToConference", "tapi/linePrepareAddToConferenceW", "tapi2.lineprepareaddtoconference"]
old-location: tapi2\lineprepareaddtoconference.htm
tech.root: tapi3
ms.assetid: e1603b36-8bcb-4665-b711-6d2b6794c963
ms.date: 08/09/2022
ms.keywords: _tapi2_lineprepareaddtoconference, linePrepareAddToConference, linePrepareAddToConference function [TAPI 2.2], linePrepareAddToConferenceA, linePrepareAddToConferenceW, tapi/linePrepareAddToConference, tapi/linePrepareAddToConferenceA, tapi/linePrepareAddToConferenceW, tapi2.lineprepareaddtoconference
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: linePrepareAddToConferenceW (Unicode) and linePrepareAddToConferenceA (ANSI)
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
 - linePrepareAddToConferenceW
 - tapi/linePrepareAddToConferenceW
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
 - linePrepareAddToConference
 - linePrepareAddToConferenceA
 - linePrepareAddToConferenceW
---

# linePrepareAddToConferenceW function


## -description

The 
<b>linePrepareAddToConference</b> function prepares an existing conference call for the addition of another party.

## -parameters

### -param hConfCall

Handle to a conference call. The application must be an owner of this call. The call state of <i>hConfCall</i> must be <i>connected</i>.

### -param lphConsultCall

Pointer to an HCALL handle. This location is then loaded with a handle identifying the consultation call to be added. Initially, the application is the sole owner of this call.

### -param lpCallParams

Pointer to a 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a> structure containing call parameters to use when establishing the consultation call. This parameter can be set to <b>NULL</b> if no special call setup parameters are desired.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_BEARERMODEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_CALLUNAVAIL, LINEERR_INVALRATE, LINEERR_CONFERENCEFULL, LINEERR_NOMEM, LINEERR_INUSE, LINEERR_NOTOWNER, LINEERR_INVALADDRESSMODE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALBEARERMODE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLPARAMS, LINEERR_RATEUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALCONFCALLHANDLE, LINEERR_STRUCTURETOOSMALL, LINEERR_INVALLINESTATE, LINEERR_USERUSERINFOTOOBIG, LINEERR_INVALMEDIAMODE, LINEERR_UNINITIALIZED.

## -remarks

If LINEERR_INVALLINESTATE is returned, the line is currently not in a state in which this operation can be performed. A list of currently valid operations can be found in the <b>dwLineFeatures</b> member (of the type 
<a href="/windows/desktop/Tapi/linefeature--constants">LINEFEATURE</a>) in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a> structure. (Calling 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetlinedevstatus">lineGetLineDevStatus</a> updates the information in 
<b>LINEDEVSTATUS</b>.)

A conference call handle can be obtained with 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetupconference">lineSetupConference</a> or with 
<a href="/windows/desktop/api/tapi/nf-tapi-linecompletetransfer">lineCompleteTransfer</a> that is resolved as a three-way conference call. The 
<b>linePrepareAddToConference</b> function typically places the existing conference call in the <i>onHoldPendingConference</i> state and creates a consultation call that can be added later to the existing conference call with 
<a href="/windows/desktop/api/tapi/nf-tapi-lineaddtoconference">lineAddToConference</a>.

The consultation call can be canceled using 
<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a>. It may also be possible for an application to swap between the consultation call and the held conference call with 
<a href="/windows/desktop/api/tapi/nf-tapi-lineswaphold">lineSwapHold</a>.





> [!NOTE]
> The tapi.h header defines linePrepareAddToConference as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/conference-ovr">Conference overview</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a>



<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineaddtoconference">lineAddToConference</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linecompletetransfer">lineCompleteTransfer</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetlinedevstatus">lineGetLineDevStatus</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetupconference">lineSetupConference</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineswaphold">lineSwapHold</a>
