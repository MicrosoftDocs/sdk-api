---
UID: NS:tapi.linecallinfo_tag
title: LINECALLINFO (tapi.h)
description: The LINECALLINFO structure contains information about a call.
helpviewer_keywords: ["*LPLINECALLINFO","LINECALLINFO","LINECALLINFO structure [TAPI 2.2]","LPLINECALLINFO","LPLINECALLINFO structure pointer [TAPI 2.2]","_tapi2_linecallinfo_str","tapi/LINECALLINFO","tapi/LPLINECALLINFO","tapi2.linecallinfo_str"]
old-location: tapi2\linecallinfo_str.htm
tech.root: tapi3
ms.assetid: b077546b-cc95-44ce-99ee-f0007fd916b2
ms.date: 12/05/2018
ms.keywords: '*LPLINECALLINFO, LINECALLINFO, LINECALLINFO structure [TAPI 2.2], LPLINECALLINFO, LPLINECALLINFO structure pointer [TAPI 2.2], _tapi2_linecallinfo_str, tapi/LINECALLINFO, tapi/LPLINECALLINFO, tapi2.linecallinfo_str'
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
req.typenames: LINECALLINFO, *LPLINECALLINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linecallinfo_tag
 - tapi/linecallinfo_tag
 - LPLINECALLINFO
 - tapi/LPLINECALLINFO
 - LINECALLINFO
 - tapi/LINECALLINFO
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
 - LINECALLINFO
---

# LINECALLINFO structure


## -description

The 
<b>LINECALLINFO</b> structure contains information about a call. This information remains relatively fixed for the duration of the call. Multiple functions use 
<b>LINECALLINFO</b>. The structure is returned by the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetcallinfo">lineGetCallInfo</a> function and the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetcallinfo">TSPI_lineGetCallInfo</a> function. If a part of the structure does change, then a 
<a href="/windows/desktop/Tapi/line-callinfo">LINE_CALLINFO</a> message is sent to the application indicating which information item has changed.

Dynamically changing information about a call, such as call progress status, is available in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallstatus">LINECALLSTATUS</a> structure, returned by a call to the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetcallstatus">lineGetCallStatus</a> function.

## -struct-fields

### -field dwTotalSize

Total size allocated to this data structure, in bytes.

### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.

### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.

### -field hLine

Handle to the line device with which this call is associated.

### -field dwLineDeviceID

Device identifier of the line device with which this call is associated.

### -field dwAddressID

Address identifier of the address on the line on which this call exists. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.

### -field dwBearerMode

Current bearer mode of the call. This member uses one of the 
<a href="/windows/desktop/Tapi/linebearermode--constants">LINEBEARERMODE_ constants</a>.

### -field dwRate

Rate of the call's data stream, in bps (bits per second).

### -field dwMediaMode

Media type of the information stream currently on the call. This is the media type as determined by the owner of the call, which is not necessarily the same as that of the last 
<a href="/windows/desktop/Tapi/line-monitormedia">LINE_MONITORMEDIA</a> message. This member is not directly affected by the LINE_MONITORMEDIA messages. This member uses the 
<a href="/windows/desktop/Tapi/linemediamode--constants">LINEMEDIAMODE_ constants</a>.

### -field dwAppSpecific

Not interpreted by the API implementation and service provider. It can be set by any owner application of this call with the 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetappspecific">lineSetAppSpecific</a> function.

### -field dwCallID

In some telephony environments, the switch or service provider can assign a unique identifier to each call. This allows the call to be tracked across transfers, forwards, or other events. The domain of these call IDs and their scope is service provider-defined. The <b>dwCallID</b> member makes this unique identifier available to the applications.

### -field dwRelatedCallID

Telephony environments that use the call ID often may find it necessary to relate one call to another. The <b>dwRelatedCallID</b> member may be used by the service provider for this purpose.

### -field dwCallParamFlags

Collection of call-related parameters when the call is outgoing. These are the same call parameters specified in 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a>, one or more of the 
<a href="/windows/desktop/Tapi/linecallparamflags--constants">LINECALLPARAMFLAGS_ constants</a>.

### -field dwCallStates

One or more of the LINECALLSTATE_ constants, that indicates the states in which the application can be notified on this call. The <b>dwCallStates</b> member is constant in 
<b>LINECALLINFO</b> and does not change depending on the call state.

### -field dwMonitorDigitModes

Various digit modes. This member is one or more of the 
<a href="/windows/desktop/Tapi/linedigitmode--constants">LINEDIGITMODE_ constants</a>, for which monitoring is currently enabled.

### -field dwMonitorMediaModes

Various media types for which monitoring is currently enabled. This member is one or more of the 
<a href="/windows/desktop/Tapi/linemediamode--constants">LINEMEDIAMODE_ constants</a>.

### -field DialParams

Dialing parameters currently in effect on the call, of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linedialparams">LINEDIALPARAMS</a>. Unless these parameters are set by either 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a> or 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetcallparams">lineSetCallParams</a>, their values are the same as the defaults used in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure.

### -field dwOrigin

Identifies where the call originated. This member can be one of the 
<a href="/windows/desktop/Tapi/linecallorigin--constants">LINECALLORIGIN_ constants</a>.

### -field dwReason

Reason why the call occurred. This member can be one of the 
<a href="/windows/desktop/Tapi/linecallreason--constants">LINECALLREASON_ constants</a>.

### -field dwCompletionID

Completion identifier for the incoming call if it is the result of a completion request that terminates. This identifier is meaningful only if <b>dwReason</b> is LINECALLREASON_CALLCOMPLETION.

### -field dwNumOwners

Number of application modules with different call handles with owner privilege for the call.

### -field dwNumMonitors

Number of application modules with different call handles with monitor privilege for the call.

### -field dwCountryCode

Country or region code of the destination party. Zero if unknown.

### -field dwTrunk

Number of the trunk over which the call is routed. This member is used for both incoming and outgoing calls. The <b>dwTrunk</b> member should be set to 0xFFFFFFFF if it is unknown.

### -field dwCallerIDFlags

Determines the validity and content of the caller, or originator, party identifier information. This member uses one of the 
<a href="/windows/desktop/Tapi/linecallpartyid--constants">LINECALLPARTYID_ constants</a>.

### -field dwCallerIDSize

Size of the caller ID number, in bytes.

### -field dwCallerIDOffset

Offset from the beginning of this structure to the variably sized field containing the caller party ID number information. The size of the field is specified by <b>dwCallerIDSize</b>.

### -field dwCallerIDNameSize

Size of the caller ID name including the null terminator, in bytes.

### -field dwCallerIDNameOffset

Offset from the beginning of this structure to the variably sized field containing the caller party ID name information. The size of the field is specified by <b>dwCallerIDNameSize</b>.

### -field dwCalledIDFlags

Determines the validity and content of the called-party ID information. The called party corresponds to the originally addressed party. This member uses one of the 
<a href="/windows/desktop/Tapi/linecallpartyid--constants">LINECALLPARTYID_ constants</a>.

### -field dwCalledIDSize

Size of the called-party ID number, in bytes.

### -field dwCalledIDOffset

Offset from the beginning of the structure to the variably sized field containing the called-party ID number information. The size of the field is specified by <b>dwCalledIDSize</b>.

### -field dwCalledIDNameSize

Size of the called-party ID name including the null terminator, in bytes.

### -field dwCalledIDNameOffset

Offset from the beginning of the structure to the variably sized field containing the called-party ID name information. The size of the field is specified by <b>dwCalledIDNameSize</b>.

### -field dwConnectedIDFlags

Determines the validity and content of the connected party ID information. The connected party is the party that was actually connected to. This may be different from the called-party ID if the call was diverted. This member uses one of the 
<a href="/windows/desktop/Tapi/linecallpartyid--constants">LINECALLPARTYID_ constants</a>.

### -field dwConnectedIDSize

Size of the connected-party ID number, in bytes.

### -field dwConnectedIDOffset

Offset from the beginning of this structure to the variably sized field containing the connected-party ID number information. The size of the field is specified by <b>dwConnectedIDSize</b>.

### -field dwConnectedIDNameSize

Size of the connected-party ID name including the null terminator, in bytes.

### -field dwConnectedIDNameOffset

Offset from the beginning of this structure to the variably sized field containing the connected-party ID name information. The size of the field is specified by <b>dwConnectedIDNameSize</b>.

### -field dwRedirectionIDFlags

Determines the validity and content of the redirection party identifier information. The redirection party identifies the address to which the session was redirected. This member uses one of the 
<a href="/windows/desktop/Tapi/linecallpartyid--constants">LINECALLPARTYID_ constants</a>.

### -field dwRedirectionIDSize

Size of the redirection-party ID number, in bytes.

### -field dwRedirectionIDOffset

Offset from the beginning of the structure to the variably sized field containing the redirection-party ID number information. The size of the field is specified by <b>dwRedirectionIDSize</b>.

### -field dwRedirectionIDNameSize

Size of the redirection-party ID name, in bytes.

### -field dwRedirectionIDNameOffset

Offset from the beginning of the structure to the variably sized field containing the redirection-party ID name information. The size of the field is specified by <b>dwRedirectionIDNameSize</b>.

### -field dwRedirectingIDFlags

Determines the validity and content of the redirecting party identifier information. The redirecting party identifies the address which redirect the session. This member uses one of the 
<a href="/windows/desktop/Tapi/linecallpartyid--constants">LINECALLPARTYID_ constants</a>.

### -field dwRedirectingIDSize

Size of the redirecting-party ID number, in bytes.

### -field dwRedirectingIDOffset

Offset from the beginning of the structure to the variably sized field containing the redirecting-party ID number information. The size of the field is specified by <b>dwRedirectingIDSize</b>.

### -field dwRedirectingIDNameSize

Size of the redirecting-party ID name including the null terminator, in bytes.

### -field dwRedirectingIDNameOffset

Offset from the beginning of the structure to the variably sized field containing the redirecting-party ID name information. The size of the field is specified by <b>dwRedirectingIDNameSize</b>.

### -field dwAppNameSize

Size of the application name field including the null terminator, in bytes.

### -field dwAppNameOffset

Offset from the beginning of the structure to the variably sized field holding the user-friendly name of the application that first originated, accepted, or answered the call. This is the name that an application can specify in 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>. If the application specifies no such name, then the application's module filename is used instead. The size of the field is specified by <b>dwAppNameSize</b>.

### -field dwDisplayableAddressSize

Size of the displayable address string including the null terminator, in bytes.

### -field dwDisplayableAddressOffset

Displayable string is used for logging purposes. The information is obtained from 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a> for functions that initiate calls. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linetranslateaddress">lineTranslateAddress</a> function returns appropriate information to be placed in this field in the <b>dwDisplayableAddressSize</b> and <b>dwDisplayableAddressOffset</b> members of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslateoutput">LINETRANSLATEOUTPUT</a> structure.

### -field dwCalledPartySize

Size of the called-party description field, in bytes.

### -field dwCalledPartyOffset

Offset from the beginning of the structure to the variably sized field that specifies the user-friendly description of the called party. This information can be specified with 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a> and can be optionally specified in the <i>lpCallParams</i> parameter whenever a new call is established. It is useful for call logging purposes. The size of the field is specified by <b>dwCalledPartySize</b>.

### -field dwCommentSize

Size of the comment field, in bytes.

### -field dwCommentOffset

Offset from the beginning of the structure to the variably sized field holding a comment about the call provided by the application that originated the call using 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a>. This information can be optionally specified in the <i>lpCallParams</i> parameter whenever a new call is established. The size of the field is specified by <b>dwCommentSize</b>.

### -field dwDisplaySize

Size of the raw display information, in bytes.

### -field dwDisplayOffset

Offset from the beginning of the structure to the variably sized field holding raw display information. Depending on the telephony environment, a service provider may extract functional information from this member pair for formatting and presentation most appropriate for this telephony configuration. The size of the field is specified by <b>dwDisplaySize</b>.

### -field dwUserUserInfoSize

Size of the user-user information, in bytes. If the user-user information is a pointer to a string, the size must include the null terminator.

### -field dwUserUserInfoOffset

Offset from the beginning of the structure to the variably sized field holding user-user information. The protocol discriminator field for the user-user information, if used, appears as the first byte of the data pointed to by <b>dwUserUserInfoOffset</b>, and is accounted for in <b>dwUserUserInfoSize</b>.

### -field dwHighLevelCompSize

Size of the high-level compatibility information, in bytes.

### -field dwHighLevelCompOffset

Offset from the beginning of the structure to the variably sized field holding high-level compatibility information. The format of this information is specified by other standards (ISDN Q.931). The size of the field is specified by <b>dwHighLevelCompSize</b>.

### -field dwLowLevelCompSize

Size of the low-level compatibility information, in bytes.

### -field dwLowLevelCompOffset

Offset from the beginning of the structure to the variably sized field holding low-level compatibility information. The format of this information is specified by other standards (ISDN Q.931). The size of the field is specified by <b>dwLowLevelCompSize</b>.

### -field dwChargingInfoSize

Size of the charging information, in bytes.

### -field dwChargingInfoOffset

Offset from the beginning of the structure to the variably sized field holding charging information. The format of this information is specified by other standards (ISDN Q.931). The size of the field is specified by <b>dwChargingInfoSize</b>.

### -field dwTerminalModesSize

Size of the current terminal modes array, in bytes.

### -field dwTerminalModesOffset

Offset from the beginning of the structure to the variably sized device field containing an array with <b>DWORD</b>-sized entries. Array entries are indexed by terminal identifiers, in the range from zero to one less than <b>dwNumTerminals</b>. Each entry in the array specifies the current terminal modes for the corresponding terminal set with the 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetterminal">lineSetTerminal</a> function for this call's media stream, as specified by one of the 
<a href="/windows/desktop/Tapi/linetermmode--constants">LINETERMMODE_ constants</a>. The size of the array is specified by <b>dwTerminalModesSize</b>.

### -field dwDevSpecificSize

Size of the device-specific field, in bytes.

### -field dwDevSpecificOffset

Offset from the beginning of the structure to the variably-sized field holding device-specific information. The size of the field is specified by <b>dwDevSpecificSize</b>.

### -field dwCallTreatment

Call treatment currently being applied on the call or that is applied when the call enters the next applicable state. Can be zero if call treatments are not supported.

### -field dwCallDataSize

Size of the application-settable call data, in bytes.

### -field dwCallDataOffset

Offset from the beginning of the structure to the application-settable call data. The size of the field is specified by <b>dwCallDataSize</b>.

### -field dwSendingFlowspecSize

Size of the quality of service information, in bytes.

### -field dwSendingFlowspecOffset

Offset from the beginning of the structure to a 
<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> structure followed by WinSock provider-specific data, equivalent to what would have been stored in <b>SendingFlowspec</b> in a 
<a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure. Specifies the quality of service currently in effect in the sending direction on the call. The provider-specific portion following the <b>FLOWSPEC</b> structure must not contain pointers to other blocks of memory, because TAPI does not know how to marshal the data pointed to by the private pointer(s) and convey it through interprocess communication to the application. The size of the field is specified by <b>dwSendingFlowspecSize</b>.

### -field dwReceivingFlowspecSize

Size of the quality of service information, in bytes.

### -field dwReceivingFlowspecOffset

Offset from the beginning of the structure to a <a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> structure followed by WinSock provider-specific data, equivalent to what would have been stored in <b>ReceivingFlowspec</b> in a <a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure. Specifies the quality of service current in effect in the receiving direction on the call. The provider-specific portion following the <b>FLOWSPEC</b> structure must not contain pointers to other blocks of memory, because TAPI does not know how to marshal the data pointed to by the private pointer(s) and convey it through interprocess communication to the application. The size of the field is specified by <b>dwReceivingFlowspecSize</b>.

### -field dwCallerIDAddressType

<a href="/windows/desktop/Tapi/lineaddresstype--constants">Address type</a> of the caller. This member of the structure is available only if the negotiated TAPI version is 3.0 or higher.

### -field dwCalledIDAddressType

<a href="/windows/desktop/Tapi/lineaddresstype--constants">Address type</a> of the called party. This member of the structure is available only if the negotiated TAPI version is 3.0 or higher.

### -field dwConnectedIDAddressType

<a href="/windows/desktop/Tapi/lineaddresstype--constants">Address type</a> of the destination to which the call was actually connected. This member of the structure is available only if the negotiated TAPI version is 3.0 or higher.

### -field dwRedirectionIDAddressType

<a href="/windows/desktop/Tapi/lineaddresstype--constants">Address type</a> of the new call destination. This member of the structure is available only if the negotiated TAPI version is 3.0 or higher.

### -field dwRedirectingIDAddressType

<a href="/windows/desktop/Tapi/lineaddresstype--constants">Address type</a> of the location which redirected the call. This member of the structure is available only if the negotiated TAPI version is 3.0 or higher.

## -remarks

Device-specific extensions should use the DevSpecific (<b>dwDevSpecificSize</b> and <b>dwDevSpecificOffset</b>) variably sized area of this data structure.

The 
<b>LINECALLINFO</b> data structure contains relatively fixed information about a call. This structure is returned with 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetcallinfo">lineGetCallInfo</a>. When information items in this data structure have changed, a LINE_CALLINFO message is sent to the application. A parameter to this message is the information item or field that changed.

The members <b>dwCallTreatment</b> through <b>dwReceivingFlowspecOffset</b> are available only to applications that open the line device with an API version of 2.0 or later.

<div class="alert"><b>Note</b>  The preferred format for specification of the contents of the <b>dwCallID</b> field and the other five similar fields (<b>dwCallerIDFlag</b>, <b>dwCallerIDSize</b>, <b>dwCallerIDOffset</b>, <b>dwCallerIDNameSize</b>, and <b>dwCallerIDNameOffset</b>) is the TAPI canonical number format. For example, a ICLID of "4258828080" received from the switch should be converted to "+1 (425) 8828080" before being placed in the 
<b>LINECALLINFO</b> structure. This standardized format facilitates searching of databases and callback functions implemented in applications.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linecallstatus">LINECALLSTATUS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedialparams">LINEDIALPARAMS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linetranslateoutput">LINETRANSLATEOUTPUT</a>



<a href="/windows/desktop/Tapi/line-callinfo">LINE_CALLINFO</a>



<a href="/windows/desktop/Tapi/line-monitormedia">LINE_MONITORMEDIA</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetcallinfo">TSPI_lineGetCallInfo</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegeneratedigits">lineGenerateDigits</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetcallinfo">lineGetCallInfo</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetcallstatus">lineGetCallStatus</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesecurecall">lineSecureCall</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetappspecific">lineSetAppSpecific</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetcallparams">lineSetCallParams</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetterminal">lineSetTerminal</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linetranslateaddress">lineTranslateAddress</a>