---
UID: NN:tapi3if.ITToneTerminalEvent
title: ITToneTerminalEvent (tapi3if.h)
description: The ITToneTerminalEvent interface contains methods that retrieve the description of tone terminal events that have occurred.
helpviewer_keywords: ["ITToneTerminalEvent","ITToneTerminalEvent interface [TAPI 2.2]","ITToneTerminalEvent interface [TAPI 2.2]","described","_tapi3_ittoneterminalevent","tapi3.ittoneterminalevent","tapi3if/ITToneTerminalEvent"]
old-location: tapi3\ittoneterminalevent.htm
tech.root: tapi3
ms.assetid: 6a5d03e9-e6d1-452a-a189-ca693a72c610
ms.date: 12/05/2018
ms.keywords: ITToneTerminalEvent, ITToneTerminalEvent interface [TAPI 2.2], ITToneTerminalEvent interface [TAPI 2.2],described, _tapi3_ittoneterminalevent, tapi3.ittoneterminalevent, tapi3if/ITToneTerminalEvent
f1_keywords:
- tapi3if/ITToneTerminalEvent
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- ITToneTerminalEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITToneTerminalEvent interface


## -description


The 
<b>ITToneTerminalEvent</b> interface contains methods that retrieve the description of tone terminal events that have occurred.

When the application's implementation of the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_TONETERMINAL</b>, the method's <i>pEvent</i> parameter is an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> pointer for the 
<b>ITToneTerminalEvent</b> interface.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes <b>TE_TONETERMINAL</b> to enable reception of tone terminal events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITToneTerminalEvent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITToneTerminalEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITToneTerminalEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittoneterminalevent-get_call">get_Call</a>
</td>
<td align="left" width="63%">
Gets the call on which the event occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittoneterminalevent-get_error">get_Error</a>
</td>
<td align="left" width="63%">
Gets the error code involved in the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittoneterminalevent-get_terminal">get_Terminal</a>
</td>
<td align="left" width="63%">
Gets the terminal on which the event occurred.

</td>
</tr>
</table> 

