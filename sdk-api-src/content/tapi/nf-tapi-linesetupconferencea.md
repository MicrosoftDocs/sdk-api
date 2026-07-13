---
UID: NF:tapi.lineSetupConferenceA
title: lineSetupConferenceA function (tapi.h)
description: The lineSetupConference function sets up a conference call for the addition of the third party. (lineSetupConferenceA)
helpviewer_keywords: ["lineSetupConferenceA", "tapi/lineSetupConferenceA"]
old-location: tapi2\linesetupconference.htm
tech.root: tapi3
ms.assetid: 13bf81c6-f7f6-4fd4-b546-15e58f7bc618
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetupconference, lineSetupConference, lineSetupConference function [TAPI 2.2], lineSetupConferenceA, lineSetupConferenceW, tapi/lineSetupConference, tapi/lineSetupConferenceA, tapi/lineSetupConferenceW, tapi2.linesetupconference
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineSetupConferenceW (Unicode) and lineSetupConferenceA (ANSI)
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
 - lineSetupConferenceA
 - tapi/lineSetupConferenceA
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
 - lineSetupConference
 - lineSetupConferenceA
 - lineSetupConferenceW
---

# lineSetupConferenceA function


## -description

The 
<b>lineSetupConference</b> function sets up a conference call for the addition of the third party.

## -parameters

### -param hCall

Handle to the Initial call that identifies the first party of a conference call. In some environments (as described in device capabilities), a call must exist to start a conference call, and the application must be an owner of this call. In other telephony environments, no call initially exists, <i>hCall</i> must be left <b>NULL</b>, and <i>hLine</i> must be specified to identify the line on which the conference call is to be initiated. The call state of <i>hCall</i> must be <i>connected</i>.

### -param hLine

Handle to the line. This handle is used to identify the line device on which to originate the conference call if <i>hCall</i> is <b>NULL</b>. The <i>hLine</i> parameter is ignored if <i>hCall</i> is non-<b>NULL</b>.

### -param lphConfCall

Pointer to an HCALL handle. This location is then loaded with a handle identifying the newly created conference call. The application is the initial sole owner of this call. The call state of <i>hConfCall</i> is not applicable.

### -param lphConsultCall

Pointer to an HCALL handle. When setting up a call for the addition of a new party, a new temporary call (consultation call) is automatically allocated. Initially, the application is the sole owner for this call.

### -param dwNumParties

Expected number of parties in the conference call. This number is passed to the service provider. The service provider is free to do as it pleases with this number: ignore it, use it as a hint to allocate the right size conference bridge inside the switch, and so on.

### -param lpCallParams

Pointer to a 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a> structure containing call parameters to use when establishing the consultation call. This parameter can be set to <b>NULL</b> if no special call setup parameters are desired.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding LINE_REPLY message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_BEARERMODEUNAVAIL, LINEERR_UNINITIALIZED, LINEERR_CALLUNAVAIL, LINEERR_INVALMEDIAMODE, LINEERR_CONFERENCEFULL, LINEERR_INVALPOINTER, LINEERR_INUSE, LINEERR_INVALRATE, LINEERR_INVALADDRESSMODE, LINEERR_NOMEM, LINEERR_INVALBEARERMODE, LINEERR_NOTOWNER, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLPARAMS, LINEERR_RATEUNAVAIL, LINEERR_INVALLINEHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALLINESTATE, LINEERR_STRUCTURETOOSMALL, LINEERR_USERUSERINFOTOOBIG.

## -remarks

If LINEERR_INVALLINESTATE is returned, the line is currently not in a state in which this operation can be performed. A list of currently valid operations can be found in the <b>dwLineFeatures</b> member (of the type 
<a href="/windows/desktop/Tapi/linefeature--constants">LINEFEATURE</a>) in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a> structure. (Calling 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetlinedevstatus">lineGetLineDevStatus</a> updates the information in 
<b>LINEDEVSTATUS</b>.) If LINEERR_INVALMEDIAMODE is returned, check for supported media types on the line in the <b>dwMediaModes</b> member in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure.

The 
<b>lineSetupConference</b> function provides two ways to establish a new conference call, depending on whether a normal two-party call is required to pre-exist or not. When setting up a conference call from an existing two-party call, the <i>hCall</i> parameter is a valid call handle that is initially added to the conference call by the 
<b>lineSetupConference</b> request; <i>hLine</i> is ignored. On switches where conference call setup does not start with an existing call, <i>hCall</i> must be <b>NULL</b> and <i>hLine</i> must be specified to identify the line device on which to initiate the conference call. In either case, a consultation call is allocated for connecting to the party that is to be added to the call. The application can then use 
<a href="/windows/desktop/api/tapi/nf-tapi-linedial">lineDial</a> to dial the address of the other party.

The conference call typically transitions into the <i>onHoldPendingConference</i> state, the consultation call into the <i>dialtone</i> state, and the initial call (if there is one) into the <i>conferenced</i> state.

A conference call can also be set up by a 
<a href="/windows/desktop/api/tapi/nf-tapi-linecompletetransfer">lineCompleteTransfer</a> that is resolved into a three-way conference. The application may be able to toggle between the consultation call and the conference call using 
<a href="/windows/desktop/api/tapi/nf-tapi-lineswaphold">lineSwapHold</a>.

A consultation call can be canceled by invoking 
<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a> on it. When dropping a consultation call, the existing conference call typically transitions back to the <i>connected</i> state. The application should observe the LINE_CALLSTATE messages to determine exactly what happens to the calls. For example, if the conference call reverts back to a regular two-party call, the conference call becomes idle and the original participant call can revert to <i>connected</i>.

If an application specifies the handle of the original call (<i>hCall</i>) in a call to the 
<a href="/windows/desktop/api/tapi/nf-tapi-lineunhold">lineUnhold</a> function, both the conference call and the consultation call typically go to idle.





> [!NOTE]
> The tapi.h header defines lineSetupConference as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/conference-ovr">Conference overview</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a>



<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linecompletetransfer">lineCompleteTransfer</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedial">lineDial</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetlinedevstatus">lineGetLineDevStatus</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineswaphold">lineSwapHold</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineunhold">lineUnhold</a>
