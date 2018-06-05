---
UID: NS:tapi.linecallinfo_tag
title: linecallinfo_tag
author: windows-sdk-content
description: The LINECALLINFO structure contains information about a call.
old-location: tapi2\linecallinfo_str.htm
old-project: Tapi
ms.assetid: b077546b-cc95-44ce-99ee-f0007fd916b2
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*LPLINECALLINFO, LINECALLINFO, LINECALLINFO structure [TAPI 2.2], LPLINECALLINFO, LPLINECALLINFO structure pointer [TAPI 2.2], _tapi2_linecallinfo_str, linecallinfo_tag, tapi/LINECALLINFO, tapi/LPLINECALLINFO, tapi2.linecallinfo_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: LINECALLINFO, *LPLINECALLINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi.h
api_name:
-	LINECALLINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# linecallinfo_tag structure


## -description


The 
<b>LINECALLINFO</b> structure contains information about a call. This information remains relatively fixed for the duration of the call. Multiple functions use 
<b>LINECALLINFO</b>. The structure is returned by the 
<a href="https://msdn.microsoft.com/e69722cb-9c45-4f1a-a855-64afa3c33276">lineGetCallInfo</a> function and the 
<a href="https://msdn.microsoft.com/9ef43928-05aa-4ec6-bc44-f07a63d8ecdf">TSPI_lineGetCallInfo</a> function. If a part of the structure does change, then a 
<a href="https://msdn.microsoft.com/eb882409-6842-434e-9f93-61cf0c11d1d0">LINE_CALLINFO</a> message is sent to the application indicating which information item has changed.

Dynamically changing information about a call, such as call progress status, is available in the 
<a href="https://msdn.microsoft.com/f056bea6-aeb0-4c18-8e3b-c1c6fd907f62">LINECALLSTATUS</a> structure, returned by a call to the 
<a href="https://msdn.microsoft.com/88bcd211-0993-4703-b43f-4e0b93e3eb7e">lineGetCallStatus</a> function.


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
<a href="https://msdn.microsoft.com/87e46ec9-ed5f-4ff5-a382-34eb164f4e66">LINEBEARERMODE_ constants</a>.


### -field dwRate

Rate of the call's data stream, in bps (bits per second).


### -field dwMediaMode

Media type of the information stream currently on the call. This is the media type as determined by the owner of the call, which is not necessarily the same as that of the last 
<a href="https://msdn.microsoft.com/1cfba455-9a15-45f3-8d56-74b8348e080e">LINE_MONITORMEDIA</a> message. This member is not directly affected by the LINE_MONITORMEDIA messages. This member uses the 
<a href="https://msdn.microsoft.com/cbb758be-3ecd-4ac4-b1b5-57136a1aad8e">LINEMEDIAMODE_ constants</a>.


### -field dwAppSpecific

Not interpreted by the API implementation and service provider. It can be set by any owner application of this call with the 
<a href="https://msdn.microsoft.com/b7d51f62-3b19-4961-8d4c-a44dc8498f14">lineSetAppSpecific</a> function.


### -field dwCallID

In some telephony environments, the switch or service provider can assign a unique identifier to each call. This allows the call to be tracked across transfers, forwards, or other events. The domain of these call IDs and their scope is service provider-defined. The <b>dwCallID</b> member makes this unique identifier available to the applications.


### -field dwRelatedCallID

Telephony environments that use the call ID often may find it necessary to relate one call to another. The <b>dwRelatedCallID</b> member may be used by the service provider for this purpose.


### -field dwCallParamFlags

Collection of call-related parameters when the call is outgoing. These are the same call parameters specified in 
<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a>, one or more of the 
<a href="https://msdn.microsoft.com/f323ec9f-5bab-4b5d-93ef-8a552ee0d591">LINECALLPARAMFLAGS_ constants</a>.


### -field dwCallStates

One or more of the LINECALLSTATE_ constants, that indicates the states in which the application can be notified on this call. The <b>dwCallStates</b> member is constant in 
<b>LINECALLINFO</b> and does not change depending on the call state.


### -field dwMonitorDigitModes

Various digit modes. This member is one or more of the 
<a href="https://msdn.microsoft.com/d603ea28-2b93-4548-bb16-78e93087f828">LINEDIGITMODE_ constants</a>, for which monitoring is currently enabled.


### -field dwMonitorMediaModes

Various media types for which monitoring is currently enabled. This member is one or more of the 
<a href="https://msdn.microsoft.com/cbb758be-3ecd-4ac4-b1b5-57136a1aad8e">LINEMEDIAMODE_ constants</a>.


### -field DialParams

Dialing parameters currently in effect on the call, of type 
<a href="https://msdn.microsoft.com/efb65462-abe5-46db-9299-97871e0d011e">LINEDIALPARAMS</a>. Unless these parameters are set by either 
<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a> or 
<a href="https://msdn.microsoft.com/c8088116-2bfc-420f-a83a-d00c7947b6e7">lineSetCallParams</a>, their values are the same as the defaults used in the 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a> structure.


### -field dwOrigin

Identifies where the call originated. This member can be one of the 
<a href="https://msdn.microsoft.com/b830a40e-62d9-4a6c-b43f-8318f30a7cd4">LINECALLORIGIN_ constants</a>.


### -field dwReason

Reason why the call occurred. This member can be one of the 
<a href="https://msdn.microsoft.com/16278146-886f-433a-afe5-64f4894b1428">LINECALLREASON_ constants</a>.


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
<a href="https://msdn.microsoft.com/e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db">LINECALLPARTYID_ constants</a>.


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
<a href="https://msdn.microsoft.com/e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db">LINECALLPARTYID_ constants</a>.


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
<a href="https://msdn.microsoft.com/e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db">LINECALLPARTYID_ constants</a>.


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
<a href="https://msdn.microsoft.com/e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db">LINECALLPARTYID_ constants</a>.


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
<a href="https://msdn.microsoft.com/e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db">LINECALLPARTYID_ constants</a>.


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
<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>. If the application specifies no such name, then the application's module filename is used instead. The size of the field is specified by <b>dwAppNameSize</b>.


### -field dwDisplayableAddressSize

Size of the displayable address string including the null terminator, in bytes.


### -field dwDisplayableAddressOffset

Displayable string is used for logging purposes. The information is obtained from 
<a href="https://msdn.microsoft.com/e7bc5604-20eb-48d8-a857-df8962c6b2ae">LINECALLPARAMS</a> for functions that initiate calls. The 
<a href="https://msdn.microsoft.com/0347d526-9596-4b42-8075-07318bf39634">lineTranslateAddress</a> function returns appropriate information to be placed in this field in the <b>dwDisplayableAddressSize</b> and <b>dwDisplayableAddressOffset</b> members of the 
<a href="https://msdn.microsoft.com/bcf094ad-8098-4e45-9131-25dbdb7e4093">LINETRANSLATEOUTPUT</a> structure.


### -field dwCalledPartySize

Size of the called-party description field, in bytes.


### -field dwCalledPartyOffset

Offset from the beginning of the structure to the variably sized field that specifies the user-friendly description of the called party. This information can be specified with 
<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a> and can be optionally specified in the <i>lpCallParams</i> parameter whenever a new call is established. It is useful for call logging purposes. The size of the field is specified by <b>dwCalledPartySize</b>.


### -field dwCommentSize

Size of the comment field, in bytes.


### -field dwCommentOffset

Offset from the beginning of the structure to the variably sized field holding a comment about the call provided by the application that originated the call using 
<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a>. This information can be optionally specified in the <i>lpCallParams</i> parameter whenever a new call is established. The size of the field is specified by <b>dwCommentSize</b>.


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
<a href="https://msdn.microsoft.com/362114d9-c5b6-4b78-bb31-811eb89fe82d">lineSetTerminal</a> function for this call's media stream, as specified by one of the 
<a href="https://msdn.microsoft.com/60af1687-8958-4918-be21-a13780c60974">LINETERMMODE_ constants</a>. The size of the array is specified by <b>dwTerminalModesSize</b>.


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
<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structure followed by WinSock provider-specific data, equivalent to what would have been stored in <b>SendingFlowspec</b> in a 
<a href="https://msdn.microsoft.com/859faa13-bd66-46ee-8452-6ff5d53d66c9">QOS</a> structure. Specifies the quality of service currently in effect in the sending direction on the call. The provider-specific portion following the <b>FLOWSPEC</b> structure must not contain pointers to other blocks of memory, because TAPI does not know how to marshal the data pointed to by the private pointer(s) and convey it through interprocess communication to the application. The size of the field is specified by <b>dwSendingFlowspecSize</b>.


### -field dwReceivingFlowspecSize

Size of the quality of service information, in bytes.


### -field dwReceivingFlowspecOffset

Offset from the beginning of the structure to a <a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structure followed by WinSock provider-specific data, equivalent to what would have been stored in <b>ReceivingFlowspec</b> in a <a href="https://msdn.microsoft.com/859faa13-bd66-46ee-8452-6ff5d53d66c9">QOS</a> structure. Specifies the quality of service current in effect in the receiving direction on the call. The provider-specific portion following the <b>FLOWSPEC</b> structure must not contain pointers to other blocks of memory, because TAPI does not know how to marshal the data pointed to by the private pointer(s) and convey it through interprocess communication to the application. The size of the field is specified by <b>dwReceivingFlowspecSize</b>.


### -field dwCallerIDAddressType


<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">Address type</a> of the caller. This member of the structure is available only if the negotiated TAPI version is 3.0 or higher.


### -field dwCalledIDAddressType


<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">Address type</a> of the called party. This member of the structure is available only if the negotiated TAPI version is 3.0 or higher.


### -field dwConnectedIDAddressType


<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">Address type</a> of the destination to which the call was actually connected. This member of the structure is available only if the negotiated TAPI version is 3.0 or higher.


### -field dwRedirectionIDAddressType


<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">Address type</a> of the new call destination. This member of the structure is available only if the negotiated TAPI version is 3.0 or higher.


### -field dwRedirectingIDAddressType


<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">Address type</a> of the location which redirected the call. This member of the structure is available only if the negotiated TAPI version is 3.0 or higher.


## -remarks



Device-specific extensions should use the DevSpecific (<b>dwDevSpecificSize</b> and <b>dwDevSpecificOffset</b>) variably sized area of this data structure.

The 
<b>LINECALLINFO</b> data structure contains relatively fixed information about a call. This structure is returned with 
<a href="https://msdn.microsoft.com/e69722cb-9c45-4f1a-a855-64afa3c33276">lineGetCallInfo</a>. When information items in this data structure have changed, a LINE_CALLINFO message is sent to the application. A parameter to this message is the information item or field that changed.

The members <b>dwCallTreatment</b> through <b>dwReceivingFlowspecOffset</b> are available only to applications that open the line device with an API version of 2.0 or later.

<div class="alert"><b>Note</b>  The preferred format for specification of the contents of the <b>dwCallID</b> field and the other five similar fields (<b>dwCallerIDFlag</b>, <b>dwCallerIDSize</b>, <b>dwCallerIDOffset</b>, <b>dwCallerIDNameSize</b>, and <b>dwCallerIDNameOffset</b>) is the TAPI canonical number format. For example, a ICLID of "4258828080" received from the switch should be converted to "+1 (425) 8828080" before being placed in the 
<b>LINECALLINFO</b> structure. This standardized format facilitates searching of databases and callback functions implemented in applications.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f056bea6-aeb0-4c18-8e3b-c1c6fd907f62">LINECALLSTATUS</a>



<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/efb65462-abe5-46db-9299-97871e0d011e">LINEDIALPARAMS</a>



<a href="https://msdn.microsoft.com/bcf094ad-8098-4e45-9131-25dbdb7e4093">LINETRANSLATEOUTPUT</a>



<a href="https://msdn.microsoft.com/eb882409-6842-434e-9f93-61cf0c11d1d0">LINE_CALLINFO</a>



<a href="https://msdn.microsoft.com/1cfba455-9a15-45f3-8d56-74b8348e080e">LINE_MONITORMEDIA</a>



<a href="https://msdn.microsoft.com/9ef43928-05aa-4ec6-bc44-f07a63d8ecdf">TSPI_lineGetCallInfo</a>



<a href="https://msdn.microsoft.com/aa407269-06be-43e2-906e-20137e4bdb89">lineGenerateDigits</a>



<a href="https://msdn.microsoft.com/e69722cb-9c45-4f1a-a855-64afa3c33276">lineGetCallInfo</a>



<a href="https://msdn.microsoft.com/88bcd211-0993-4703-b43f-4e0b93e3eb7e">lineGetCallStatus</a>



<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>



<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a>



<a href="https://msdn.microsoft.com/b12a5734-0638-4bb0-8f25-ca27d28e528b">lineSecureCall</a>



<a href="https://msdn.microsoft.com/b7d51f62-3b19-4961-8d4c-a44dc8498f14">lineSetAppSpecific</a>



<a href="https://msdn.microsoft.com/c8088116-2bfc-420f-a83a-d00c7947b6e7">lineSetCallParams</a>



<a href="https://msdn.microsoft.com/362114d9-c5b6-4b78-bb31-811eb89fe82d">lineSetTerminal</a>



<a href="https://msdn.microsoft.com/0347d526-9596-4b42-8075-07318bf39634">lineTranslateAddress</a>
 

 

