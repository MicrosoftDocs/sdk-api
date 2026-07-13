---
UID: NF:tapi.lineMakeCallA
title: lineMakeCallA function (tapi.h)
description: The lineMakeCall function places a call on the specified line to the specified destination address. Optionally, call parameters can be specified if anything but default call setup parameters are requested. (lineMakeCallA)
helpviewer_keywords: ["lineMakeCallA", "tapi/lineMakeCallA"]
old-location: tapi2\linemakecall.htm
tech.root: tapi3
ms.assetid: a7dc9cdc-3cc3-4b6a-98c8-e141402c781e
ms.date: 12/05/2018
ms.keywords: _tapi2_linemakecall, lineMakeCall, lineMakeCall function [TAPI 2.2], lineMakeCallA, lineMakeCallW, tapi/lineMakeCall, tapi/lineMakeCallA, tapi/lineMakeCallW, tapi2.linemakecall
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineMakeCallW (Unicode) and lineMakeCallA (ANSI)
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
 - lineMakeCallA
 - tapi/lineMakeCallA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ras-tapi32-l1-1-1.dll
 - Tapi32.dll
api_name:
 - lineMakeCall
 - lineMakeCallA
 - lineMakeCallW
---

# lineMakeCallA function


## -description

The 
<b>lineMakeCall</b> function places a call on the specified line to the specified destination address. Optionally, call parameters can be specified if anything but default call setup parameters are requested.

## -parameters

### -param hLine

Handle to the open line device on which a call is to be originated.

### -param lphCall

Pointer to an HCALL handle. The handle is only valid after the 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is received by the application indicating that the 
<b>lineMakeCall</b> function successfully completed. Use this handle to identify the call when invoking other telephony operations on the call. The application is initially the sole owner of this call. This handle is void if the function returns an error (synchronously or asynchronously by the reply message).

### -param lpszDestAddress

Pointer to the destination address. This follows the standard dialable number format. This pointer can be <b>NULL</b> for non-dialed addresses (as with a hot phone) or when all dialing is performed using 
<a href="/windows/desktop/api/tapi/nf-tapi-linedial">lineDial</a>. In the latter case, 
<b>lineMakeCall</b> allocates an available call appearance that would typically remain in the <b>dialtone</b> state until dialing begins. Service providers that have inverse multiplexing capabilities can allow an application to specify multiple addresses at once.

### -param dwCountryCode

Country or region code of the called party. If a value of 0 is specified, a default is used by the implementation.

### -param lpCallParams

Pointer to a 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a> structure. This structure allows the application to specify how it wants the call to be set up. If <b>NULL</b> is specified, a default 3.1 kHz voice call is established and an arbitrary origination address on the line is selected. This structure allows the application to select elements such as the call's bearer mode, data rate, expected media mode, origination address, blocking of caller ID information, and dialing parameters.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_ADDRESSBLOCKED, LINEERR_INVALLINEHANDLE, LINEERR_BEARERMODEUNAVAIL, LINEERR_INVALLINESTATE, LINEERR_CALLUNAVAIL, LINEERR_INVALMEDIAMODE, LINEERR_DIALBILLING, LINEERR_INVALPARAM, LINEERR_DIALDIALTONE, LINEERR_INVALPOINTER, LINEERR_DIALPROMPT, LINEERR_INVALRATE, LINEERR_DIALQUIET, LINEERR_NOMEM, LINEERR_INUSE, LINEERR_OPERATIONFAILED, LINEERR_INVALADDRESS, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALADDRESSID, LINEERR_RATEUNAVAIL, LINEERR_INVALADDRESSMODE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALBEARERMODE, LINEERR_STRUCTURETOOSMALL, LINEERR_INVALCALLPARAMS, LINEERR_UNINITIALIZED, LINEERR_INVALCOUNTRYCODE, LINEERR_USERUSERINFOTOOBIG.

## -remarks

If LINEERR_INVALLINESTATE is returned, the line is currently not in a state in which this operation can be performed. A list of currently valid operations can be found in the <b>dwLineFeatures</b> member (of the type LINEFEATURE_) in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a> structure. Calling 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetlinedevstatus">lineGetLineDevStatus</a> updates the information in 
<b>LINEDEVSTATUS</b>. If LINEERR_DIALBILLING, LINEERR_DIALQUIET, LINEERR_DIALDIALTONE, or LINEERR_DIALPROMPT is returned, none of the actions otherwise performed by 
<b>lineMakeCall</b> have occurred; for example, none of the dialable address prior to the offending character has been dialed, no hookswitch state has changed, and so on.

After dialing has completed, several 
<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a> messages are usually sent to the application to notify it about the progress of the call. No generally valid sequence of call-state transitions is specified, as no single fixed sequence of transitions can be guaranteed in practice. A typical sequence can cause a call to transition from <i>dialtone</i>, <i>dialing</i>, <i>proceeding</i>, <i>ringback</i>, to <i>connected</i>. With non-dialed lines, the call can typically transition directly to <i>connected</i> state.

An application has the option to specify an originating address on the specified line device. A service provider that models all stations on a switch as addresses on a single line device allows the application to originate calls from any of these stations using 
<b>lineMakeCall</b>.

The call parameters allow the application to make non-voice calls or request special call setup options that are not available by default.

An application can partially dial using 
<b>lineMakeCall</b> and continue dialing using 
<a href="/windows/desktop/api/tapi/nf-tapi-linedial">lineDial</a>. For more information on partial dialing, see <a href="/windows/desktop/api/tapi/nf-tapi-linedial">lineDial</a> and <a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemakecall">TSPI_lineMakeCall</a>.  To abandon a call attempt, use 
<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a>.

After 
<b>lineMakeCall</b> returns a success reply message to the application, a LINE_CALLSTATE message is sent to the application to indicate the current state of the call. This state is not necessarily LINECALLSTATE_DIALTONE.

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.

<div class="alert"><b>Caution</b>  TAPI will write the returned data to the buffer referenced by lphCall when the LINE_REPLY message is returned. This means that the buffer must remain valid until the LINE_REPLY message is returned; otherwise, data corruption and exceptions may occur.
</div>
<div> </div>




> [!NOTE]
> The tapi.h header defines lineMakeCall as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/win32/tapi/address-ovr#dialable-addresses">Dialable addresses</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a>



<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a>



<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedial">lineDial</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetlinedevstatus">lineGetLineDevStatus</a>
