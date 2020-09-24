---
UID: NF:tapi.lineSetTerminal
title: lineSetTerminal function (tapi.h)
description: The lineSetTerminal function enables an application to specify which terminal information related to the specified line, address, or call is to be routed.
helpviewer_keywords: ["_tapi2_linesetterminal","lineSetTerminal","lineSetTerminal function [TAPI 2.2]","tapi/lineSetTerminal","tapi2.linesetterminal"]
old-location: tapi2\linesetterminal.htm
tech.root: tapi3
ms.assetid: 362114d9-c5b6-4b78-bb31-811eb89fe82d
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetterminal, lineSetTerminal, lineSetTerminal function [TAPI 2.2], tapi/lineSetTerminal, tapi2.linesetterminal
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineSetTerminal
 - tapi/lineSetTerminal
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
 - lineSetTerminal
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
<a href="/windows/desktop/Tapi/linecallselect--constants">LINECALLSELECT_ Constants</a>.

### -param dwTerminalModes

Class of low-level events to be routed to the given terminal. This parameter uses one or more of the 
<a href="/windows/desktop/Tapi/linetermmode--constants">LINETERMMODE_ Constants</a>.

### -param dwTerminalID

Device identifier of the terminal device where the given events are to be routed. Terminal identifiers are small integers in the range of zero to one less than <b>dwNumTerminals</b>, where <b>dwNumTerminals</b>, and the terminal modes each terminal is capable of handling, are returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevcaps">lineGetDevCaps</a>. 




These terminal identifiers have no relation to other device identifiers and are defined by the service provider using device capabilities.

### -param bEnable

If <b>TRUE</b>, <i>dwTerminalID</i> is valid and the specified event classes are routed to or from that terminal. If <b>FALSE</b>, these events are not routed to or from the terminal device with identifier equal to <i>dwTerminalID</i>.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESSID, LINEERR_NOMEM, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSELECT, LINEERR_OPERATIONFAILED, LINEERR_INVALLINEHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALTERMINALID, LINEERR_UNINITIALIZED, LINEERR_INVALTERMINALMODE.

## -remarks

An application can use this function to route certain classes of low-level line events to the specified terminal device or to suppress the routing of these events. For example, voice can be routed to an audio I/O device (headset), lamps and display events can be routed to the local phone device, and button events and ringer events can be suppressed altogether.

This function can be called at any time, even when a call is active on the given line device. This allows a user to switch from using the local phone set to another audio I/O device. This function can be called multiple times to route the same events to multiple terminals simultaneously. To reroute events to a different terminal, the application should first disable routing to the existing terminal and then route the events to the new terminal.

Terminal identifier assignments are made by the line's service provider. Device capabilities indicate only which terminal identifiers the service provider has available. Service providers that do not support this type of event routing would indicate that they have no terminal devices (<b>dwNumTerminals</b> in 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> would be zero).

Invoking 
<b>lineSetTerminal</b> on a line or address affects all existing calls on that line or address, but does not affect calls on other addresses. It also sets the default for future calls on that line or address. A line or address that has multiple connected calls active at one time can have different routing in effect for each call.

Disabling the routing of low-level events to a terminal when these events are not currently routed to or from that terminal does not necessarily generate an error so long as the function succeeds (the specified events are not routed to or from that terminal).

TAPI routes call progress tones and messages to the same location as set by the 
<b>lineSetTerminal</b> function for "media". For example, if audio signals are going to the phone, then so will busy signals (analog) or Q.931 messages indicating busy (digital).

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevcaps">lineGetDevCaps</a>