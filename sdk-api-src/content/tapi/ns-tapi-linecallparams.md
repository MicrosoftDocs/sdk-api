---
UID: NS:tapi.linecallparams_tag
title: LINECALLPARAMS (tapi.h)
description: The LINECALLPARAMS structure describes parameters supplied when making calls using the lineMakeCall and TSPI_lineMakeCall functions. The LINECALLPARAMS structure is also used as a parameter in other operations, such as the lineOpen function.
helpviewer_keywords: ["*LPLINECALLPARAMS","LINECALLPARAMS","LINECALLPARAMS structure [TAPI 2.2]","LPLINECALLPARAMS","LPLINECALLPARAMS structure pointer [TAPI 2.2]","_tapi2_linecallparams_str","tapi/LINECALLPARAMS","tapi/LPLINECALLPARAMS","tapi2.linecallparams_str"]
old-location: tapi2\linecallparams_str.htm
tech.root: tapi3
ms.assetid: e7bc5604-20eb-48d8-a857-df8962c6b2ae
ms.date: 12/05/2018
ms.keywords: '*LPLINECALLPARAMS, LINECALLPARAMS, LINECALLPARAMS structure [TAPI 2.2], LPLINECALLPARAMS, LPLINECALLPARAMS structure pointer [TAPI 2.2], _tapi2_linecallparams_str, tapi/LINECALLPARAMS, tapi/LPLINECALLPARAMS, tapi2.linecallparams_str'
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
req.typenames: LINECALLPARAMS, *LPLINECALLPARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linecallparams_tag
 - tapi/linecallparams_tag
 - LPLINECALLPARAMS
 - tapi/LPLINECALLPARAMS
 - LINECALLPARAMS
 - tapi/LINECALLPARAMS
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
 - LINECALLPARAMS
---

# LINECALLPARAMS structure


## -description

The 
<b>LINECALLPARAMS</b> structure describes parameters supplied when making calls using the 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a> and 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemakecall">TSPI_lineMakeCall</a> functions. The 
<b>LINECALLPARAMS</b> structure is also used as a parameter in other operations, such as the 
<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a> function.

The comments to the right of the syntax block indicate the default values used when this structure is not provided to 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a>.

## -struct-fields

### -field dwTotalSize

Total size allocated to this data structure, in bytes. This size should be big enough to hold all the fixed and variably sized portions of this data structure.

### -field dwBearerMode

Bearer mode for the call. This member uses one of the 
<a href="/windows/desktop/Tapi/linebearermode--constants">LINEBEARERMODE_ constants</a>. 




If <b>dwBearerMode</b> is zero, the default value is LINEBEARERMODE_VOICE.

### -field dwMinRate

Minimum data rate requested for the call's data stream, in bps (bits per second).

### -field dwMaxRate

Maximum data rate requested for the call's data stream, in bps (bits per second). When making a call, the service provider attempts to provide the highest available rate in the requested range (<b>dwMinRate</b> to <b>dwMaxRate</b>). If a specific data rate is required, both <b>dwMinRate</b> and <b>dwMaxRate</b> should be set to that value. If an application works best with one rate but is able to degrade to lower rates, the application should specify these as the maximum and minimum rates, respectively. If <b>dwMaxRate</b> is zero, the default value is as specified by the <b>dwMaxRate</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure. This is the maximum rate supported by the device.

### -field dwMediaMode

Expected media type of the call. This member uses one of the 
<a href="/windows/desktop/Tapi/linemediamode--constants">LINEMEDIAMODE_ constants</a>. 




If <b>dwMediaMode</b> is zero, the default value is LINEMEDIAMODE_INTERACTIVEVOICE.

### -field dwCallParamFlags

Collection of Boolean call-setup parameters. This member uses one or more of the 
<a href="/windows/desktop/Tapi/linecallparamflags--constants">LINECALLPARAMFLAGS_ constants</a>.

### -field dwAddressMode

Mode by which the originating address is specified.  This member uses one of the 
<a href="/windows/desktop/Tapi/lineaddressmode--constants">LINEADDRESSMODE_ constants</a>.

<div class="alert"><b>Note</b>  The <b>dwAddressMode</b> member cannot be LINEADDRESSMODE_ADDRESSID for the 
<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a> function call. However, this restriction does not apply to <a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a>.</div>
<div> </div>

### -field dwAddressID

Address identifier of the originating address if <b>dwAddressMode</b> is set to LINEADDRESSMODE_ADDRESSID. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.

### -field DialParams

Dial parameters to be used on this call, of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linedialparams">LINEDIALPARAMS</a>. When a value of 0 is specified for this field, the default value for the field is used as indicated in the <b>DefaultDialParams</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure. If a nonzero value is specified for a field that is outside the range specified by the corresponding fields in <b>MinDialParams</b> and <b>MaxDialParams</b> in the 
<b>LINEDEVCAPS</b> structure, the nearest value within the valid range is used instead.

### -field dwOrigAddressSize

Size of the originating address field, in bytes.

### -field dwOrigAddressOffset

Offset from the beginning of the structure to the variably sized field holding the originating address. The format of this address is dependent on the <b>dwAddressMode</b> member. The size of the field is specified by <b>dwOrigAddressSize</b>.

### -field dwDisplayableAddressSize

Size of the displayable string including the <b>null</b> terminator, in bytes.

### -field dwDisplayableAddressOffset

Displayable string used for logging purposes. The content of these members is recorded in the <b>dwDisplayableAddressOffset</b> and <b>dwDisplayableAddressSize</b> members of the call's LINECALLINFO message. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linetranslateaddress">lineTranslateAddress</a> function returns appropriate information to be placed in this field in the <b>dwDisplayableAddressSize</b> and <b>dwDisplayableAddressOffset</b> members of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslateoutput">LINETRANSLATEOUTPUT</a> structure. The size of the field is specified by <b>dwDisplayableAddressSize</b>.

### -field dwCalledPartySize

Size of the called-party information, in bytes.

### -field dwCalledPartyOffset

Offset from the beginning of the structure to the variably sized field holding called-party information. This information can be specified by the application that makes the call and is made available in the call's information structure for logging purposes. The format of this field is that of <b>dwStringFormat</b>, as specified in 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>. The size of the field is specified by <b>dwCalledPartySize</b>.

### -field dwCommentSize

Size of the call comment field, in bytes.

### -field dwCommentOffset

Offset from the beginning of the structure to the variably sized field holding comments about the call. This information can be specified by the application that makes the call and is made available in the call's information structure for logging purposes. The format of this field is that of <b>dwStringFormat</b>, as specified in 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>. The size of the field is specified by <b>dwCommentSize</b>.

### -field dwUserUserInfoSize

Size of the user-user information including the <b>null</b> terminator, in bytes.

### -field dwUserUserInfoOffset

Offset from the beginning of the structure to the variably sized field holding user-user information. The protocol discriminator field for the user-user information, if required, should appear as the first byte of the data pointed to by <b>dwUserUserInfoOffset</b>, and must be accounted for in <b>dwUserUserInfoSize</b>.

### -field dwHighLevelCompSize

Size of the high-level compatibility information, in bytes.

### -field dwHighLevelCompOffset

Offset from the beginning of the structure to the variably sized field holding high-level compatibility information. The size of the field is specified by <b>dwHighLevelCompSize</b>.

### -field dwLowLevelCompSize

Size of the low-level compatibility information, in bytes.

### -field dwLowLevelCompOffset

Offset from the beginning of the structure to the variably sized field holding low-level compatibility information. The size of the field is specified by <b>dwLowLevelCompSize</b>.

### -field dwDevSpecificSize

Size of the device-specific information, in bytes.

### -field dwDevSpecificOffset

Offset from the beginning of the structure to the variably sized field holding device-specific information. The size of the field is specified by <b>dwDevSpecificSize</b>.

### -field dwPredictiveAutoTransferStates

<a href="/windows/desktop/Tapi/linecallstate--constants">LINECALLSTATE_ constants</a>, entry into which causes the call to be blind-transferred to the specified target address. Set to zero if automatic transfer is not desired.

### -field dwTargetAddressSize

Size of the target dialable address string including the <b>null</b> terminator, in bytes.

### -field dwTargetAddressOffset

Offset from the beginning of the structure to a string specifying the target dialable address (not <b>dwAddressID</b>); used in the case of certain automatic actions. In the case of predictive dialing, specifies the address to which the call should be automatically transferred. The size of the string is specified by <b>dwTargetAddressSize</b>. 




This is essentially the same string that would be passed to 
<a href="/windows/desktop/api/tapi/nf-tapi-lineblindtransfer">lineBlindTransfer</a> if automatic transfer were not being used. Set to zero if automatic transfer is not desired. In the case of a No Hold Conference, specifies the address that should be conferenced to the call. In the case of a One Step Transfer, specifies the address to dial on the consultation call.

### -field dwSendingFlowspecSize

Size of the quality of service information, in bytes.

### -field dwSendingFlowspecOffset

Offset from the beginning of the structure to a 
<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> structure followed by WinSock provider-specific data, equivalent to what would have been stored in <b>SendingFlowspec</b> in a 
<a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure. Specifies the quality of service desired in the sending direction on the call. The provider-specific portion following the <b>FLOWSPEC</b> structure must not contain pointers to other blocks of memory, because TAPI does not know how to marshal the data pointed to by the private pointer(s) and convey it through interprocess communication to the application. The size of the field is specified by <b>dwSendingFlowspecSize</b>.

### -field dwReceivingFlowspecSize

Size of the quality of service information, in bytes.

### -field dwReceivingFlowspecOffset

Offset from the beginning of the structure to a <a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> structure followed by WinSock provider-specific data, equivalent to what would have been stored in <b>ReceivingFlowspec</b> in a <a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure. Specifies the quality of service desired in the receiving direction on the call. The provider-specific portion following the <b>FLOWSPEC</b> structure must not contain pointers to other blocks of memory, because TAPI does not know how to marshal the data pointed to by the private pointer(s) and convey it through interprocess communication to the application. The size of the field is specified by <b>dwReceivingFlowspecSize</b>.

### -field dwDeviceClassSize

Size of the device class string including the <b>null</b> terminator, in bytes.

### -field dwDeviceClassOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that indicates the device class of the device whose configuration is specified in <i>DeviceConfig</i>. Valid device class strings are the same as those specified for the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetid">lineGetID</a> function. The size of the string is specified by <b>dwDeviceClassSize</b>.

### -field dwDeviceConfigSize

Size of the device configuration data, in bytes.

### -field dwDeviceConfigOffset

Offset from the beginning of the structure to the opaque configuration data structure. This value is returned in the <b>dwStringSize</b> member in the 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> structure returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">lineGetDevConfig</a>. If the size is zero, the default device configuration is used. This allows the application to set the device configuration before the call is initiated. The size of the field is specified by <b>dwDeviceConfigSize</b>.

### -field dwCallDataSize

Size of the application-settable call data, in bytes.

### -field dwCallDataOffset

Offset from the beginning of the structure to the application-settable call data to be initially attached to the call. The size of the field is specified by <b>dwCallDataSize</b>.

### -field dwNoAnswerTimeout

Number of seconds, after the completion of dialing, that the call should be allowed to wait in the PROCEEDING or RINGBACK states, before it is automatically abandoned by the service provider with a LINECALLSTATE_DISCONNECTED and LINEDISCONNECTMODE_NOANSWER. A value of 0 indicates that the application does not desire automatic call abandonment.

### -field dwCallingPartyIDSize

Size of the calling-party ID string including the <b>null</b> terminator, in bytes, including the <b>null</b>-terminating character.

### -field dwCallingPartyIDOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that specifies the identity of the party placing the call. If the content of the identifier is acceptable and a path is available, the service provider passes the identifier along to the called party to indicate the identity of the calling party. The size of the field is specified by <b>dwCallingPartyIDSize</b>.

### -field dwAddressType

<a href="/windows/desktop/Tapi/lineaddresstype--constants">Address type</a> used for the call. This member of the structure is available only if the negotiated TAPI version is 3.0 or higher.

## -remarks

Device-specific extensions should use the DevSpecific (<b>dwDevSpecificSize</b> and <b>dwDevSpecificOffset</b>) variably sized area of this data structure.

This structure is used as a parameter to 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a> when setting up a call. Its fields allow the application to specify the quality of service requested from the network as well as a variety of ISDN call-setup parameters. If no 
<b>LINECALLPARAMS</b> structure is supplied to 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a>, a default POTS voice-grade call is requested with the default values listed above.

<div class="alert"><b>Note</b>  The fields <b>DialParams</b> through <b>dwDevSpecificOffset</b> are ignored when an <i>lpCallParams</i> parameter is specified with the 
<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a> function.</div>
<div> </div>
The members <b>dwPredictiveAutoTransferStates</b> through <b>dwCallingPartyIDOffset</b> are available only to applications that open the line device with an API version of 2.0 or later.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedialparams">LINEDIALPARAMS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linetranslateoutput">LINETRANSLATEOUTPUT</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemakecall">TSPI_lineMakeCall</a>



<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineblindtransfer">lineBlindTransfer</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">lineGetDevConfig</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetid">lineGetID</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linetranslateaddress">lineTranslateAddress</a>