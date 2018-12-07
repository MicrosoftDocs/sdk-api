---
UID: NF:tapi.lineSetMediaControl
title: lineSetMediaControl function
author: windows-sdk-content
description: The lineSetMediaControl function enables and disables control actions on the media stream associated with the specified line, address, or call.
old-location: tapi2\linesetmediacontrol.htm
tech.root: tapi
ms.assetid: 5a4fc83a-6bc9-4081-b374-ddb912fb2242
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_tapi2_linesetmediacontrol, lineSetMediaControl, lineSetMediaControl function [TAPI 2.2], tapi/lineSetMediaControl, tapi2.linesetmediacontrol"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineSetMediaControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineSetMediaControl function


## -description


The 
<b>lineSetMediaControl</b> function enables and disables control actions on the media stream associated with the specified line, address, or call. Media control actions can be triggered by the detection of specified digits, media types, custom tones, and call states.


## -parameters




### -param hLine

Handle to an open line device.


### -param dwAddressID

Address identifier on the given open line device. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.


### -param hCall

Handle to a call. The application must be an owner of the call. The call state of <i>hCall</i> can be any state.


### -param dwSelect

Whether the media control requested is associated with a single call, is the default for all calls on an address, or is the default for all calls on a line. This parameter one and only one of the 
<a href="https://msdn.microsoft.com/f19a41bc-403a-4d4b-ab85-240a73514ebb">LINECALLSELECT_ Constants</a>.


### -param lpDigitList

Pointer to the array that contains the digits that are to trigger media control actions, of type 
<a href="https://msdn.microsoft.com/d31cd365-d6a6-4595-8202-87113035d807">LINEMEDIACONTROLDIGIT</a>. Each time a digit in the digit list is detected, the specified media control action is carried out on the call's media stream. 




Valid digits for pulse mode are '0' through '9'. Valid digits for DTMF mode are '0' through '9', 'A', 'B', 'C', 'D', '*', '#'.


### -param dwDigitNumEntries

Number of entries in the <i>lpDigitList</i>.


### -param lpMediaList

Pointer to an array with entries of type 
<a href="https://msdn.microsoft.com/5515d510-3827-4da6-975c-ff191bb0ab4e">LINEMEDIACONTROLMEDIA</a>. The array has <i>dwMediaNumEntries</i> entries. Each entry contains a media type to be monitored, media-type specific information (such as duration), and a media control field. If a media type in the list is detected, the corresponding media control action is performed on the call's media stream.


### -param dwMediaNumEntries

Number of entries in <i>lpMediaList</i>.


### -param lpToneList

Pointer to an array with entries of type 
<a href="https://msdn.microsoft.com/0513d580-aaf1-412c-adbf-9342b74025ee">LINEMEDIACONTROLTONE</a>. The array has <i>dwToneNumEntries</i> entries. Each entry contains a description of a tone to be monitored, duration of the tone, and a media-control field. If a tone in the list is detected, the corresponding media control action is performed on the call's media stream.


### -param dwToneNumEntries

Number of entries in <i>lpToneList</i>.


### -param lpCallStateList

Pointer to an array with entries of type 
<a href="https://msdn.microsoft.com/c0768c2a-3015-41af-b32f-0b228a0f2ee6">LINEMEDIACONTROLCALLSTATE</a>. The array has <i>dwCallStateNumEntries</i> entries. Each entry contains a call state and a media control action. Whenever the given call transitions into one of the call states in the list, the corresponding media control action is invoked.


### -param dwCallStateNumEntries

Number of entries in <i>lpCallStateList</i>.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESSID, LINEERR_NOMEM, LINEERR_INVALCALLHANDLE, LINEERR_NOTOWNER, LINEERR_INVALCALLSELECT, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATELIST, LINEERR_OPERATIONFAILED, LINEERR_INVALDIGITLIST, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALLINEHANDLE, LINEERR_UNINITIALIZED, LINEERR_INVALMEDIALIST, LINEERR_INVALPOINTER, LINEERR_INVALTONELIST.




## -remarks



The 
<b>lineSetMediaControl</b> function is considered successful if media control has been correctly initiated, not when any media control has taken effect. Media control in progress is changed or is canceled by calling this function again with either different parameters or <b>NULL</b>s. If one or more of the parameters <i>lpDigitList</i>, <i>lpMediaList</i>, <i>lpToneList</i>, and <i>lpCallStateList</i> are <b>NULL</b>, then the corresponding digit, media type, tone, or call state-triggered media control is disabled. To modify just a portion of the media control parameters while leaving the remaining settings in effect, the application should invoke 
<b>lineSetMediaControl</b>, supplying the previous parameters for those portions that must remain in effect and new parameters for those parts that are to be modified.

If <i>hCall</i> is selected and the call terminates or the application deallocates its handle, media control on that call is canceled.

All applications that are owners of the call are in principle allowed to make media control requests on the call. Only a single media control request can be outstanding on a call across all applications that own the call. Each time 
<b>lineSetMediaControl</b> is called, the new request overrides any media control then in effect on the call, whether set by the calling application or any other owning application.

Depending on the service provider and other activities that compete for such resources, the number of simultaneous detections that can be made can vary over time. If service provider resources are overcommitted, the LINEERR_RESOURCEUNAVAIL error is returned.

Whether or not media control is supported by the service provider is a device capability.




## -see-also




<a href="https://msdn.microsoft.com/c0768c2a-3015-41af-b32f-0b228a0f2ee6">LINEMEDIACONTROLCALLSTATE</a>



<a href="https://msdn.microsoft.com/d31cd365-d6a6-4595-8202-87113035d807">LINEMEDIACONTROLDIGIT</a>



<a href="https://msdn.microsoft.com/5515d510-3827-4da6-975c-ff191bb0ab4e">LINEMEDIACONTROLMEDIA</a>



<a href="https://msdn.microsoft.com/0513d580-aaf1-412c-adbf-9342b74025ee">LINEMEDIACONTROLTONE</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

