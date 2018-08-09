---
UID: NF:tapi.lineSetTerminal
title: lineSetTerminal function
author: windows-sdk-content
description: The lineSetTerminal function enables an application to specify which terminal information related to the specified line, address, or call is to be routed.
old-location: tapi2\linesetterminal.htm
old-project: tapi
ms.assetid: 362114d9-c5b6-4b78-bb31-811eb89fe82d
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: "_tapi2_linesetterminal, lineSetTerminal, lineSetTerminal function [TAPI 2.2], tapi/lineSetTerminal, tapi2.linesetterminal"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FLICK_POINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineSetTerminal
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineSetTerminal function


## -description


The 
<b>lineSetTerminal</b> function enables an application to specify which terminal information related to the specified line, address, or call is to be routed. The 
<b>lineSetTerminal</b> function can be used while calls are in progress on the line to allow an application to route these events to different devices as required.


## -parameters




### -param hLine

Handle to an open line device.


### -param dwAddressID

Address on the given open line device. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.


### -param hCall

Handle to a call. The call state of <i>hCall</i> can be any state, if <i>dwSelect</i> is CALL.


### -param dwSelect

Whether the terminal setting is requested for the line, the address, or just the specified call. If line or address is specified, events either apply to the line or address itself or serve as a default initial setting for all new calls on the line or address. This parameter uses one of the 
<a href="https://msdn.microsoft.com/f19a41bc-403a-4d4b-ab85-240a73514ebb">LINECALLSELECT_ Constants</a>.


### -param dwTerminalModes

Class of low-level events to be routed to the given terminal. This parameter uses one or more of the 
<a href="https://msdn.microsoft.com/60af1687-8958-4918-be21-a13780c60974">LINETERMMODE_ Constants</a>.


### -param dwTerminalID

Device identifier of the terminal device where the given events are to be routed. Terminal identifiers are small integers in the range of zero to one less than <b>dwNumTerminals</b>, where <b>dwNumTerminals</b>, and the terminal modes each terminal is capable of handling, are returned by 
<a href="https://msdn.microsoft.com/c0900c5b-8791-4653-8bfc-d32e51d10c50">lineGetDevCaps</a>. 




These terminal identifiers have no relation to other device identifiers and are defined by the service provider using device capabilities.


### -param bEnable

If <b>TRUE</b>, <i>dwTerminalID</i> is valid and the specified event classes are routed to or from that terminal. If <b>FALSE</b>, these events are not routed to or from the terminal device with identifier equal to <i>dwTerminalID</i>.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESSID, LINEERR_NOMEM, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSELECT, LINEERR_OPERATIONFAILED, LINEERR_INVALLINEHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALTERMINALID, LINEERR_UNINITIALIZED, LINEERR_INVALTERMINALMODE.




## -remarks



An application can use this function to route certain classes of low-level line events to the specified terminal device or to suppress the routing of these events. For example, voice can be routed to an audio I/O device (headset), lamps and display events can be routed to the local phone device, and button events and ringer events can be suppressed altogether.

This function can be called at any time, even when a call is active on the given line device. This allows a user to switch from using the local phone set to another audio I/O device. This function can be called multiple times to route the same events to multiple terminals simultaneously. To reroute events to a different terminal, the application should first disable routing to the existing terminal and then route the events to the new terminal.

Terminal identifier assignments are made by the line's service provider. Device capabilities indicate only which terminal identifiers the service provider has available. Service providers that do not support this type of event routing would indicate that they have no terminal devices (<b>dwNumTerminals</b> in 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a> would be zero).

Invoking 
<b>lineSetTerminal</b> on a line or address affects all existing calls on that line or address, but does not affect calls on other addresses. It also sets the default for future calls on that line or address. A line or address that has multiple connected calls active at one time can have different routing in effect for each call.

Disabling the routing of low-level events to a terminal when these events are not currently routed to or from that terminal does not necessarily generate an error so long as the function succeeds (the specified events are not routed to or from that terminal).

TAPI routes call progress tones and messages to the same location as set by the 
<b>lineSetTerminal</b> function for "media". For example, if audio signals are going to the phone, then so will busy signals (analog) or Q.931 messages indicating busy (digital).




## -see-also




<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/c0900c5b-8791-4653-8bfc-d32e51d10c50">lineGetDevCaps</a>
 

 

