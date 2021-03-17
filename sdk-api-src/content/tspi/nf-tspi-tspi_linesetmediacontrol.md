---
UID: NF:tspi.TSPI_lineSetMediaControl
title: TSPI_lineSetMediaControl function (tspi.h)
description: The TSPI_lineSetMediaControl function enables and disables control actions on the media stream associated with the specified line, address, or call.
helpviewer_keywords: ["TSPI_lineSetMediaControl","TSPI_lineSetMediaControl function [TAPI 2.2]","_tspi_tspi_linesetmediacontrol","tspi.tspi_linesetmediacontrol","tspi/TSPI_lineSetMediaControl"]
old-location: tspi\tspi_linesetmediacontrol.htm
tech.root: tapi3
ms.assetid: e9273bd6-8dc3-4b45-bf0e-a1a10d78a604
ms.date: 12/05/2018
ms.keywords: TSPI_lineSetMediaControl, TSPI_lineSetMediaControl function [TAPI 2.2], _tspi_tspi_linesetmediacontrol, tspi.tspi_linesetmediacontrol, tspi/TSPI_lineSetMediaControl
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
 - TSPI_lineSetMediaControl
 - tspi/TSPI_lineSetMediaControl
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
 - TSPI_lineSetMediaControl
---

# TSPI_lineSetMediaControl function


## -description

The 
<b>TSPI_lineSetMediaControl</b> function enables and disables control actions on the media stream associated with the specified line, address, or call. Media control actions can be triggered by the detection of specified digits, media types, custom tones, and call states. The new specified media controls replace all the ones that were in effect for this line, address, or call prior to this request.

## -parameters

### -param hdLine

The handle to a line.

### -param dwAddressID

An address on the given open line device. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades. TAPI does not validate this parameter when this function is called.

### -param hdCall

The handle to a call. The call state of <i>hdCall</i> can be any state.

### -param dwSelect

Specifies whether media control is requested is associated with a single call, is the default for all calls on an address, or is the default for all calls on a line. This parameter uses the following 
<a href="/windows/desktop/Tapi/linecallselect--constants">LINECALLSELECT_ constants</a>.

### -param lpDigitList

A pointer to the array that contains the digits that are to trigger media control actions, of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linemediacontroldigit">LINEMEDIACONTROLDIGIT</a>. Each time a digit listed in the digit list is detected, the specified media control action is carried out on the call's media stream. 




Valid digits for pulse mode are '0' through '9'. Valid digits for DTMF mode are '0' through '9', 'A', 'B', 'C', 'D', '*', '#'.

### -param dwDigitNumEntries

The number of entries in the <i>lpDigitList</i>. TAPI does not validate this parameter when this function is called.

### -param lpMediaList

A pointer to an array with entries of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linemediacontrolmedia">LINEMEDIACONTROLMEDIA</a>. The array has <i>dwMediaNumEntries</i> entries. Each entry contains a media type to be monitored, media-type specific information (such as duration), and a media control field. If a media type in the list is detected, the corresponding media control action is performed on the call's media stream.

### -param dwMediaNumEntries

The number of entries in <i>lpMediaList</i>. TAPI does not validate this parameter when this function is called.

### -param lpToneList

A pointer to an array with entries of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linemediacontroltone">LINEMEDIACONTROLTONE</a>. The array has <i>dwToneNumEntries</i> entries. Each entry contains a description of a tone to be monitored, duration of the tone, and a media control field. If a tone in the list is detected, the corresponding media control action is performed on the call's media stream.

### -param dwToneNumEntries

The number of entries in <i>lpToneList</i>. TAPI does not validate this parameter when this function is called.

### -param lpCallStateList

A pointer to an array with entries of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linemediacontrolcallstate">LINEMEDIACONTROLCALLSTATE</a>. The array has <i>dwCallStateNumEntries</i> entries. Each entry contains a call state and a media control action.

### -param dwCallStateNumEntries

The number of entries in <i>lpCallStateList</i>. TAPI does not validate this parameter when this function is called.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALADDRESSID, LINEERR_INVALPOINTER, LINEERR_INVALCALLHANDLE, LINEERR_INVALTONELIST, LINEERR_INVALCALLSELECT, LINEERR_NOMEM, LINEERR_INVALCALLSTATELIST, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALDIGITLIST, LINEERR_OPERATIONFAILED, LINEERR_INVALLINEHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALMEDIALIST.

## -remarks

This function returns zero (success) when media control is correctly initiated, not when any media control takes effect. Media control in progress is changed or is canceled when this function is called again with either different parameters or <b>NULL</b>s.

Only a single media control request can be outstanding on a call at one time. A request replaces any that may be outstanding.

Depending on the service provider and other activities that compete for such resources, the amount of simultaneous detections that can be made can vary over time. If service provider resources are overcommitted, it returns LINEERR_RESOURCEUNAVAIL.

Whether or not media control is supported by the service provider is a device capability indicated in 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>.

Each time 
<b>TSPI_lineSetMediaControl</b> is called, the new request overrides any media control currently in effect. If one or more of the parameters <i>lpDigitList</i>, <i>lpMediaList</i>, <i>lpToneList</i>, and <i>lpCallStateList</i> are <b>NULL</b>, the corresponding digit, media type, tone, or call state-triggered media control is disabled. To modify just a portion of the media control parameters while leaving the remaining settings in effect, the application should invoke 
<b>TSPI_lineSetMediaControl</b> supplying the previous parameters for those portions that must remain in effect, and new parameters for those parts that are to be modified.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/Tapi/linedigitmode--constants">LINEDIGITMODE_ Constants</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linemediacontrolcallstate">LINEMEDIACONTROLCALLSTATE</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linemediacontroldigit">LINEMEDIACONTROLDIGIT</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linemediacontrolmedia">LINEMEDIACONTROLMEDIA</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linemediacontroltone">LINEMEDIACONTROLTONE</a>



<a href="/windows/desktop/Tapi/linemediamode--constants">LINEMEDIAMODE_ Constants</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetdevcaps">TSPI_lineGetDevCaps</a>