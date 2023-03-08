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
 - ITToneTerminalEvent
 - tapi3if/ITToneTerminalEvent
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
 - ITToneTerminalEvent
---

# ITToneTerminalEvent interface


## -description

The 
<b>ITToneTerminalEvent</b> interface contains methods that retrieve the description of tone terminal events that have occurred.

When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_TONETERMINAL</b>, the method's <i>pEvent</i> parameter is an 
<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> pointer for the 
<b>ITToneTerminalEvent</b> interface.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes <b>TE_TONETERMINAL</b> to enable reception of tone terminal events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b>ITToneTerminalEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITToneTerminalEvent</b> also has these types of members:

