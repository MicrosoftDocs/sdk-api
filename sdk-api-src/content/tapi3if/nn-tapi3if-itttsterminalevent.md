---
UID: NN:tapi3if.ITTTSTerminalEvent
title: ITTTSTerminalEvent (tapi3if.h)
description: The ITTTSTerminalEvent interface contains methods that retrieve the description of Text-to-Speech (TTS) terminal events that have occurred.
helpviewer_keywords: ["ITTTSTerminalEvent","ITTTSTerminalEvent interface [TAPI 2.2]","ITTTSTerminalEvent interface [TAPI 2.2]","described","_tapi3_itttsterminalevent","tapi3.itttsterminalevent","tapi3if/ITTTSTerminalEvent"]
old-location: tapi3\itttsterminalevent.htm
tech.root: tapi3
ms.assetid: 0375d6e4-cd9f-4245-abf5-1b200af79848
ms.date: 12/05/2018
ms.keywords: ITTTSTerminalEvent, ITTTSTerminalEvent interface [TAPI 2.2], ITTTSTerminalEvent interface [TAPI 2.2],described, _tapi3_itttsterminalevent, tapi3.itttsterminalevent, tapi3if/ITTTSTerminalEvent
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITTTSTerminalEvent
 - tapi3if/ITTTSTerminalEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITTTSTerminalEvent
---

# ITTTSTerminalEvent interface


## -description

The 
<b>ITTTSTerminalEvent</b> interface contains methods that retrieve the description of Text-to-Speech (TTS) terminal events that have occurred.

When the application's implementation of the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_TTSTERMINAL</b>, the method's <i>pEvent</i> parameter is an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> pointer for the 
<b>ITTTSTerminalEvent</b> interface.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes <b>TE_TTSTERMINAL</b> to enable reception of Text-to-Speech terminal events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTTSTerminalEvent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITTTSTerminalEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITTTSTerminalEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itttsterminalevent-get_call">get_Call</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface pointer for the call object involved in the terminal event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itttsterminalevent-get_error">get_Error</a>
</td>
<td align="left" width="63%">
Gets the error code involved in the terminal event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itttsterminalevent-get_terminal">get_Terminal</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface pointer for the terminal object involved in the terminal event.

</td>
</tr>
</table>

