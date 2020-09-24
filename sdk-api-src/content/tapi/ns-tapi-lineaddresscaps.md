---
UID: NS:tapi.lineaddresscaps_tag
title: LINEADDRESSCAPS (tapi.h)
description: The LINEADDRESSCAPS structure describes the capabilities of a specified address. The lineGetAddressCaps function and the TSPI_lineGetAddressCaps function return the LINEADDRESSCAPS structure.
helpviewer_keywords: ["*LPLINEADDRESSCAPS","LINEADDRESSCAPS","LINEADDRESSCAPS structure [TAPI 2.2]","LPLINEADDRESSCAPS","LPLINEADDRESSCAPS structure pointer [TAPI 2.2]","_tapi2_lineaddresscaps_str","tapi/LINEADDRESSCAPS","tapi/LPLINEADDRESSCAPS","tapi2.lineaddresscaps_str"]
old-location: tapi2\lineaddresscaps_str.htm
tech.root: tapi3
ms.assetid: c1fe1aaf-2f50-4423-bacf-6a3cf218a809
ms.date: 12/05/2018
ms.keywords: '*LPLINEADDRESSCAPS, LINEADDRESSCAPS, LINEADDRESSCAPS structure [TAPI 2.2], LPLINEADDRESSCAPS, LPLINEADDRESSCAPS structure pointer [TAPI 2.2], _tapi2_lineaddresscaps_str, tapi/LINEADDRESSCAPS, tapi/LPLINEADDRESSCAPS, tapi2.lineaddresscaps_str'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LINEADDRESSCAPS, *LPLINEADDRESSCAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineaddresscaps_tag
 - tapi/lineaddresscaps_tag
 - LPLINEADDRESSCAPS
 - tapi/LPLINEADDRESSCAPS
 - LINEADDRESSCAPS
 - tapi/LINEADDRESSCAPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEADDRESSCAPS
---

# LINEADDRESSCAPS structure


## -description

The 
<b>LINEADDRESSCAPS</b> structure describes the capabilities of a specified address. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetaddresscaps">lineGetAddressCaps</a> function and the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetaddresscaps">TSPI_lineGetAddressCaps</a> function return the 
<b>LINEADDRESSCAPS</b> structure.

## -struct-fields

### -field dwTotalSize

Total size allocated to this data structure, in bytes.

### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.

### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.

### -field dwLineDeviceID

Device identifier of the line device with which this address is associated.

### -field dwAddressSize

Size of the address field, in bytes.

### -field dwAddressOffset

Offset from the beginning of the structure to the variably sized address field. The size of the field is specified by <b>dwAddressSize</b>.

### -field dwDevSpecificSize

Size of the device-specific field, in bytes.

### -field dwDevSpecificOffset

Offset from the beginning of the structure to the variably sized device-specific field. The size of the field is specified by <b>dwDevSpecificSize</b>.

### -field dwAddressSharing

Sharing mode of the address. This member can be one of the 
<a href="/windows/desktop/Tapi/lineaddresssharing--constants">LINEADDRESSSHARING_ Constants</a>.

### -field dwAddressStates

Address states changes for which the application may get notified in the LINE_ADDRESSSTATE message. This member uses one or more of the 
<a href="/windows/desktop/Tapi/lineaddressstate--constants">LINEADDRESSSTATE_ constants</a>.

### -field dwCallInfoStates

Call information elements that are meaningful for all calls on this address. An application may get notified about changes in some of these states in 
<a href="/windows/desktop/Tapi/line-callinfo">LINE_CALLINFO</a> messages. This member uses one or more of the 
<a href="/windows/desktop/Tapi/linecallinfostate--constants">LINECALLINFOSTATE_ constants</a>.

### -field dwCallerIDFlags

Party identifier information types that can be provided for calls on this address. The caller is the originator of the session. One or more of the 
<a href="/windows/desktop/Tapi/linecallpartyid--constants">LINECALLPARTYID_ constants</a>.

### -field dwCalledIDFlags

Party identifier information types that can be provided for calls on this address. Here, "called" refers to the original destination. One or more of the 
<a href="/windows/desktop/Tapi/linecallpartyid--constants">LINECALLPARTYID_ constants</a>.

### -field dwConnectedIDFlags

Party identifier information types that can be provided for calls on this address. One or more of the 
<a href="/windows/desktop/Tapi/linecallpartyid--constants">LINECALLPARTYID_ constants</a>.

### -field dwRedirectionIDFlags

Party identifier information types that can be provided for calls on this address. Here, "redirection" is the new destination. One or more of the 
<a href="/windows/desktop/Tapi/linecallpartyid--constants">LINECALLPARTYID_ constants</a>.

### -field dwRedirectingIDFlags

Party identifier information types that can be provided for calls on this address. Here, "redirecting" is the address which invoked redirection. One or more of the 
<a href="/windows/desktop/Tapi/linecallpartyid--constants">LINECALLPARTYID_ constants</a>.

### -field dwCallStates

Call states that can be reported for calls on this address. This member uses one or more of the 
<a href="/windows/desktop/Tapi/linecallstate--constants">LINECALLSTATE_ constants</a>.

### -field dwDialToneModes

Dial tone modes that can be reported for calls made on this address. This member is meaningful only if the <i>dialtone</i> call state can be reported. This member uses one or more of the 
<a href="/windows/desktop/Tapi/linedialtonemode--constants">LINEDIALTONEMODE_ constants</a>.

### -field dwBusyModes

Busy modes that can be reported for calls made on this address. This member is meaningful only if the <i>busy</i> call state can be reported. This member uses one or more of the 
<a href="/windows/desktop/Tapi/linebusymode--constants">LINEBUSYMODE_ constants</a>.

### -field dwSpecialInfo

Special information types that can be reported for calls made on this address. This member is meaningful only if the <i>specialInfo</i> call state can be reported. This member uses one or more of the 
<a href="/windows/desktop/Tapi/linespecialinfo--constants">LINESPECIALINFO_ constants</a>.

### -field dwDisconnectModes

Disconnect modes that can be reported for calls made on this address. This member is meaningful only if the <i>disconnected</i> call state can be reported. This member uses one or more of the 
<a href="/windows/desktop/Tapi/linedisconnectmode--constants">LINEDISCONNECTMODE_ constants</a>.

### -field dwMaxNumActiveCalls

Maximum number of active call appearances that the address can handle. This number does not include calls on hold or calls on hold pending transfer or conference.

### -field dwMaxNumOnHoldCalls

Maximum number of call appearances at the address that can be on hold.

### -field dwMaxNumOnHoldPendingCalls

Maximum number of call appearances at the address that can be on hold pending transfer or conference.

### -field dwMaxNumConference

Maximum number of parties that can join a single conference call on this address.

### -field dwMaxNumTransConf

Number of parties (including "self") that can be added in a conference call that is initiated as a generic consultation call using 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetuptransfer">lineSetupTransfer</a>.

### -field dwAddrCapFlags

Packed bit flags that describe a variety of address capabilities. This member uses one or more of the 
<a href="/windows/desktop/Tapi/lineaddrcapflags--constants">LINEADDRCAPFLAGS_ constants</a>.

### -field dwCallFeatures

Switching capabilities or features available for all calls on this address using the 
<a href="/windows/desktop/Tapi/linecallfeature--constants">LINECALLFEATURE_ Constants</a>. This member represents the call-related features that may possibly be available on an address (static availability as opposed to dynamic availability). Invoking a supported feature requires the call to be in the proper state and the underlying line device to be opened in a compatible mode. A zero in a bit position indicates that the corresponding feature is never available. A one indicates that the corresponding feature may be available if the application has the right privileges to the call and the call is in the appropriate state for the operation to be meaningful. This member allows an application to discover which call features can be (and which can never be) supported by the address.

### -field dwRemoveFromConfCaps

Address's capabilities for removing calls from a conference call. This member uses one of the 
<a href="/windows/desktop/Tapi/lineremovefromconf--constants">LINEREMOVEFROMCONF_ constants</a>.

### -field dwRemoveFromConfState

Uses the LINECALLSTATE_ constants to specify the state of the call after it has been removed from a conference call.

### -field dwTransferModes

Address's capabilities for resolving transfer requests. This member uses one of the 
<a href="/windows/desktop/Tapi/linetransfermode--constants">LINETRANSFERMODE_ constants</a>.

### -field dwParkModes

Different call park modes available at this address. This member uses one of the 
<a href="/windows/desktop/Tapi/lineparkmode--constants">LINEPARKMODE_ constants</a>.

### -field dwForwardModes

Different modes of forwarding available for this address. This member uses the 
<a href="/windows/desktop/Tapi/lineforwardmode--constants">LINEFORWARDMODE_ constants</a>.

### -field dwMaxForwardEntries

Maximum number of entries that can be passed to 
<a href="/windows/desktop/api/tapi/nf-tapi-lineforward">lineForward</a> in the <i>lpForwardList</i> parameter.

### -field dwMaxSpecificEntries

Maximum number of entries in the <i>lpForwardList</i> parameter passed to 
<a href="/windows/desktop/api/tapi/nf-tapi-lineforward">lineForward</a> that can contain forwarding instructions based on a specific caller ID (selective call forwarding). This member is zero if selective call forwarding is not supported.

### -field dwMinFwdNumRings

Minimum number of rings that can be set to determine when a call is officially considered "no answer."

### -field dwMaxFwdNumRings

Maximum number of rings that can be set to determine when a call is officially considered "no answer." If this number of rings cannot be set, then <b>dwMinFwdNumRings</b> and <b>dwMaxNumRings</b> are equal.

### -field dwMaxCallCompletions

Maximum number of concurrent call completion requests that can be outstanding on this line device. Zero implies that call completion is not available.

### -field dwCallCompletionConds

Different call conditions under which call completion can be requested. This member uses one or more of the LINECALLCOMPLCOND_ constants.

### -field dwCallCompletionModes

Way in which the call can be completed. This member uses one of the LINECALLCOMPLMODE_ constants.

### -field dwNumCompletionMessages

Number of call completion messages that can be selected from when using the LINECALLCOMPLMODE_MESSAGE option. Individual messages are identified by values in the range zero through one less than <b>dwNumCompletionMessages</b>.

### -field dwCompletionMsgTextEntrySize

Size of each of the call completion text descriptions specified by <b>dwCompletionMsgTextSize</b> and <b>dwCompletionMsgTextOffset</b>, in bytes.

### -field dwCompletionMsgTextSize

Size of the call completion text, in bytes.

### -field dwCompletionMsgTextOffset

Offset from the beginning of this data structure to the variably sized field containing descriptive text about each of the call completion messages. Each message is <b>dwCompletionMsgTextEntrySize</b> bytes long. The string format of these textual descriptions is indicated by <b>dwStringFormat</b> in the line's device capabilities. The size of the field is specified by <b>dwCompletionMsgTextSize</b>.

### -field dwAddressFeatures

Features available for this address using the 
<a href="/windows/desktop/Tapi/lineaddrfeature--constants">LINEADDRFEATURE_ Constants</a>. Invoking a supported feature requires the address to be in the proper state and the underlying line device to be opened in a compatible mode. A zero in a bit position indicates that the corresponding feature is never available. A one indicates that the corresponding feature may be available if the address is in the appropriate state for the operation to be meaningful. This member allows an application to discover which address features can be (and which can never be) supported by the address.

### -field dwPredictiveAutoTransferStates

Call state or states upon which a call made by a predictive dialer can be set to automatically transfer the call to another address; one or more of the 
<a href="/windows/desktop/Tapi/linecallstate--constants">LINECALLSTATE_ Constants</a>. The value 0 indicates automatic transfer based on call state is unavailable.

### -field dwNumCallTreatments

Number of entries in the array of 
<a href="/windows/desktop/api/tapi/ns-tapi-linecalltreatmententry">LINECALLTREATMENTENTRY</a> structures delimited by <b>dwCallTreatmentListSize</b> and <b>dwCallTreatmentListOffset</b>.

### -field dwCallTreatmentListSize

Size of the call treatment array, in bytes.

### -field dwCallTreatmentListOffset

Offset from the beginning of the structure to an array of 
<a href="/windows/desktop/api/tapi/ns-tapi-linecalltreatmententry">LINECALLTREATMENTENTRY</a> structures the specify the call treatments supported on the address (that can be selected using 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetcalltreatment">lineSetCallTreatment</a>). The value is <b>dwNumCallTreatments</b> times SIZEOF(LINECALLTREATMENTENTRY). The size of the field is specified by <b>dwCallTreatmentListSize</b>.

### -field dwDeviceClassesSize

Size of the list of supported device classes, in bytes.

### -field dwDeviceClassesOffset

Offset from the beginning of the structure to a string consisting of the device class identifiers supported on this address for use with 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetid">lineGetID</a>. The elements are separated by <b>null</b> characters, and the last class identifier is followed by two <b>null</b> characters. The size of the field is specified by <b>dwDeviceClassesSize</b>.

### -field dwMaxCallDataSize

Maximum number of bytes that an application can set in 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> using 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetcalldata">lineSetCallData</a>.

### -field dwCallFeatures2

Additional switching capabilities or features available for all calls on this address using the 
<a href="/windows/desktop/Tapi/linecallfeature2--constants">LINECALLFEATURE2_ Constants</a>. It is an extension of the <b>dwCallFeatures</b> member.

### -field dwMaxNoAnswerTimeout

Maximum value in seconds that can be set in the <b>dwNoAnswerTimeout</b> member in 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a> when making a call. A value of 0 indicates that automatic abandonment of unanswered calls is not supported by the service provider, or that the timeout value is not adjustable by applications.

### -field dwConnectedModes

LINECONNECTEDMODE_ values that can appear in the <b>dwCallStateMode</b> member of 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallstatus">LINECALLSTATUS</a> and in 
<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a> messages for calls on this address.

### -field dwOfferingModes

LINEOFFERINGMODE_ values that can appear in the <b>dwCallStateMode</b> member of 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallstatus">LINECALLSTATUS</a> and in LINE_CALLSTATE messages for calls on this address.

### -field dwAvailableMediaModes

Media types (modes) that can be invoked on new calls created on this address, when the <b>dwAddressFeatures</b> member indicates that new calls are possible. If this member is zero, it indicates that the service provider either does not know or cannot indicate which media types are available, in which case any or all of the media types indicated in the <b>dwMediaModes</b> member in 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> may be available.

## -remarks

Device-specific extensions should use the <b>DevSpecific</b> (<b>dwDevSpecificSize</b> and <b>dwDevSpecificOffset</b>) variably sized area of this data structure.

Older applications are compiled without this member in the 
<b>LINEADDRESSCAPS</b> structure, and using a SIZEOF(LINEADDRESSCAPS) smaller than the new size. The application passes in a <i>dwAPIVersion</i> parameter with the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetaddresscaps">lineGetAddressCaps</a> function, which can be used for guidance by TAPI in handling this situation. If the application passes in a <b>dwTotalSize</b> member less than the size of the fixed portion of the structure as defined in the <b>dwAPIVersion</b> member specified, LINEERR_STRUCTURETOOSMALL is returned. If sufficient memory has been allocated by the application, before calling 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetaddresscaps">TSPI_lineGetAddressCaps</a>, TAPI sets the <b>dwNeededSize</b> and <b>dwUsedSize</b> members to the fixed size of the structure as it existed in the specified API version.

New service providers (that support the new API version) must examine the API version passed in. If the API version is less than the highest version supported by the provider, the service provider must not fill in fields not supported in older API versions, as these would fall in the variable portion of the older structure.

New applications must be cognizant of the API version negotiated, and not examine the contents of fields in the fixed portion beyond the original end of the fixed portion of the structure for the negotiated API version. 

The members <b>dwPredictiveAutoTransferStates</b> through <b>dwAvailableMediaModes</b> are available only to applications that request an API version of 2.0 or later when calling 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetaddresscaps">lineGetAddressCaps</a>.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineaddressstatus">LINEADDRESSSTATUS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallstatus">LINECALLSTATUS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecalltreatmententry">LINECALLTREATMENTENTRY</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedialparams">LINEDIALPARAMS</a>



<a href="/windows/desktop/Tapi/line-addressstate">LINE_ADDRESSSTATE</a>



<a href="/windows/desktop/Tapi/line-callinfo">LINE_CALLINFO</a>



<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a>



<a href="/windows/desktop/Tapi/line-linedevstate">LINE_LINEDEVSTATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetaddresscaps">TSPI_lineGetAddressCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linecompletecall">lineCompleteCall</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineforward">lineForward</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegeneratedigits">lineGenerateDigits</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetaddresscaps">lineGetAddressCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetid">lineGetID</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetcalldata">lineSetCallData</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetcalltreatment">lineSetCallTreatment</a>