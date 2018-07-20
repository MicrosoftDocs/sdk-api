---
UID: NF:tspi.TSPI_lineSetMediaControl
title: TSPI_lineSetMediaControl function
author: windows-sdk-content
description: The TSPI_lineSetMediaControl function enables and disables control actions on the media stream associated with the specified line, address, or call.
old-location: tspi\tspi_linesetmediacontrol.htm
old-project: tapi
ms.assetid: e9273bd6-8dc3-4b45-bf0e-a1a10d78a604
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: TSPI_lineSetMediaControl, TSPI_lineSetMediaControl function [TAPI 2.2], _tspi_tspi_linesetmediacontrol, tspi.tspi_linesetmediacontrol, tspi/TSPI_lineSetMediaControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: AAAccountingData
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineSetMediaControl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
<a href="https://msdn.microsoft.com/f19a41bc-403a-4d4b-ab85-240a73514ebb">LINECALLSELECT_ constants</a>.


### -param lpDigitList

A pointer to the array that contains the digits that are to trigger media control actions, of type 
<a href="https://msdn.microsoft.com/d31cd365-d6a6-4595-8202-87113035d807">LINEMEDIACONTROLDIGIT</a>. Each time a digit listed in the digit list is detected, the specified media control action is carried out on the call's media stream. 




Valid digits for pulse mode are '0' through '9'. Valid digits for DTMF mode are '0' through '9', 'A', 'B', 'C', 'D', '*', '#'.


### -param dwDigitNumEntries

The number of entries in the <i>lpDigitList</i>. TAPI does not validate this parameter when this function is called.


### -param lpMediaList

A pointer to an array with entries of type 
<a href="https://msdn.microsoft.com/5515d510-3827-4da6-975c-ff191bb0ab4e">LINEMEDIACONTROLMEDIA</a>. The array has <i>dwMediaNumEntries</i> entries. Each entry contains a media type to be monitored, media-type specific information (such as duration), and a media control field. If a media type in the list is detected, the corresponding media control action is performed on the call's media stream.


### -param dwMediaNumEntries

The number of entries in <i>lpMediaList</i>. TAPI does not validate this parameter when this function is called.


### -param lpToneList

A pointer to an array with entries of type 
<a href="https://msdn.microsoft.com/0513d580-aaf1-412c-adbf-9342b74025ee">LINEMEDIACONTROLTONE</a>. The array has <i>dwToneNumEntries</i> entries. Each entry contains a description of a tone to be monitored, duration of the tone, and a media control field. If a tone in the list is detected, the corresponding media control action is performed on the call's media stream.


### -param dwToneNumEntries

The number of entries in <i>lpToneList</i>. TAPI does not validate this parameter when this function is called.


### -param lpCallStateList

A pointer to an array with entries of type 
<a href="https://msdn.microsoft.com/c0768c2a-3015-41af-b32f-0b228a0f2ee6">LINEMEDIACONTROLCALLSTATE</a>. The array has <i>dwCallStateNumEntries</i> entries. Each entry contains a call state and a media control action.


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
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>.

Each time 
<b>TSPI_lineSetMediaControl</b> is called, the new request overrides any media control currently in effect. If one or more of the parameters <i>lpDigitList</i>, <i>lpMediaList</i>, <i>lpToneList</i>, and <i>lpCallStateList</i> are <b>NULL</b>, the corresponding digit, media type, tone, or call state-triggered media control is disabled. To modify just a portion of the media control parameters while leaving the remaining settings in effect, the application should invoke 
<b>TSPI_lineSetMediaControl</b> supplying the previous parameters for those portions that must remain in effect, and new parameters for those parts that are to be modified.




## -see-also




<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/d603ea28-2b93-4548-bb16-78e93087f828">LINEDIGITMODE_ Constants</a>



<a href="https://msdn.microsoft.com/c0768c2a-3015-41af-b32f-0b228a0f2ee6">LINEMEDIACONTROLCALLSTATE</a>



<a href="https://msdn.microsoft.com/d31cd365-d6a6-4595-8202-87113035d807">LINEMEDIACONTROLDIGIT</a>



<a href="https://msdn.microsoft.com/5515d510-3827-4da6-975c-ff191bb0ab4e">LINEMEDIACONTROLMEDIA</a>



<a href="https://msdn.microsoft.com/0513d580-aaf1-412c-adbf-9342b74025ee">LINEMEDIACONTROLTONE</a>



<a href="https://msdn.microsoft.com/cbb758be-3ecd-4ac4-b1b5-57136a1aad8e">LINEMEDIAMODE_ Constants</a>



<a href="https://msdn.microsoft.com/6c5a668e-9a9a-4a7a-98e9-bd8ec4b819b2">TSPI_lineGetDevCaps</a>
 

 

