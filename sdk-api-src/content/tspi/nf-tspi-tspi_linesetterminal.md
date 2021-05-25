---
UID: NF:tspi.TSPI_lineSetTerminal
title: TSPI_lineSetTerminal function (tspi.h)
description: The TSPI_lineSetTerminal function enables TAPI to specify to which terminal information related to the specified line, address, or call is to be routed.
helpviewer_keywords: ["TSPI_lineSetTerminal","TSPI_lineSetTerminal function [TAPI 2.2]","_tspi_tspi_linesetterminal","tspi.tspi_linesetterminal","tspi/TSPI_lineSetTerminal"]
old-location: tspi\tspi_linesetterminal.htm
tech.root: tapi3
ms.assetid: 106451b0-4491-472d-b73a-5d8333f0a372
ms.date: 12/05/2018
ms.keywords: TSPI_lineSetTerminal, TSPI_lineSetTerminal function [TAPI 2.2], _tspi_tspi_linesetterminal, tspi.tspi_linesetterminal, tspi/TSPI_lineSetTerminal
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
 - TSPI_lineSetTerminal
 - tspi/TSPI_lineSetTerminal
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
 - TSPI_lineSetTerminal
---

# TSPI_lineSetTerminal function


## -description

The 
<b>TSPI_lineSetTerminal</b> function enables TAPI to specify to which terminal information related to the specified line, address, or call is to be routed. This operation can be used while calls are in progress on the line, to allow events to be routed to different devices as required.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdLine

The handle to a line.

### -param dwAddressID

An address on the given open line device. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades. TAPI does not validate this parameter when this function is called.

### -param hdCall

The handle to a call. The call state can be any state (if <i>dwSelect</i> is LINECALLSELECT_CALL).

### -param dwSelect

Specifies whether the terminal setting is requested for the line, the address, or just the specified call. If line or address is specified, events either apply to the line or address itself or serve as a default initial setting for all new calls on the line or address. This parameter uses one of the 
<a href="/windows/desktop/Tapi/linecallselect--constants">LINECALLSELECT_ constants</a>.

### -param dwTerminalModes

The class(es) of low level events to be routed to the given terminal. Use one of the 
<a href="/windows/desktop/Tapi/linetermmode--constants">LINETERMMODE_ Constants</a> for this parameter.

### -param dwTerminalID

The device identifier of the terminal device where the given events are to be routed. Terminal identifiers are small integers in the range from 0 through <b>dwNumTerminals</b> minus one, where <b>dwNumTerminals</b> and the terminal modes each terminal is capable of handling are indicated by the service provider in 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>. 




<div class="alert"><b>Note</b>  These terminal identifiers have no relation to other device identifiers and are defined by the service provider through device capabilities. TAPI does not validate this parameter when this function is called.</div>
<div> </div>

### -param bEnable

If <b>TRUE</b>, <i>dwTerminalID</i> is valid and the specified event classes are routed to or from that terminal. If <b>FALSE</b>, these events are not routed to or from the <i>dwTerminalID</i>. TAPI does not validate this parameter when this function is called.

## -returns

Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALLINEHANDLE, LINEERR_INVALTERMINALID, LINEERR_INVALADDRESSID, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALCALLHANDLE, LINEERR_NOMEM, LINEERR_INVALCALLSELECT, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALTERMINALMODE, LINEERR_OPERATIONFAILED.

## -remarks

The service provider returns LINEERR_RESOURCEUNAVAIL if the operation cannot be completed because of resource overcommitment or if too many terminals are set, due either to hardware limitations or to service provider/device driver limitations.

TAPI can use this operation to route certain classes of low-level line events to the specified terminal device, or to suppress the routing of these events altogether. For example, voice can be routed to a separate audio I/O device (headset), lamps and display events can be routed to the local phone device, and button events and ringer events can be suppressed altogether.

Call progress tones and/or messages get routed to the same place as media. For example, if audio signals are going to the phone, then so are busy signals (analog) or Q.931 messages indicating busy (digital).

The service provider must determine whether the combinations of <i>dwSelect</i> and <i>dwTerminalModes</i> are legal.

This operation can be called any time, even when a call is active on the given line device. This, for example, allows a user to switch from using the local phone set to another audio I/O device.

This function can be called multiple times to route the same events to multiple terminals simultaneously. To reroute events to a different terminal, TAPI recommends that the application first disable routing to the existing terminal and next route the events to the new terminal. However, the service provider should make its best effort to accommodate the application's requests in any sequence.

Terminal identifier assignments are made by the service provider, and 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> indicates which terminal identifiers the service provider has available. Service providers that don't support this type of event routing indicate that they have no terminal devices (<b>dwNumTerminals</b> in 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> is set to zero).

<b>LineSetTerminal</b> on a line or address affects all existing calls on that line or address, but does not affect calls on other addresses. It also sets the default for future calls on that line or address. A line or address that has multiple connected calls active at any one time can have different routing in effect for each call.

Disabling the routing of low-level events to a terminal when these events are not currently routed to or from that terminal is not required to generate an error so long as after the function succeeds, the specified events are not routed to or from that terminal.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/Tapi/linecallselect--constants">LINECALLSELECT_ Constants</a>



<a href="/windows/desktop/Tapi/linetermmode--constants">LINETERMMODE_ Constants</a>