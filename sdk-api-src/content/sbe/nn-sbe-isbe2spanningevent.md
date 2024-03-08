---
UID: NN:sbe.ISBE2SpanningEvent
title: ISBE2SpanningEvent (sbe.h)
description: Implements in-band spanning events for the Stream Buffer Engine, version 2 (SBE2). An in-band spanning event is an in-band event that can be recorded as part of the state information in a stream.
helpviewer_keywords: ["ISBE2SpanningEvent","ISBE2SpanningEvent interface [Microsoft TV Technologies]","ISBE2SpanningEvent interface [Microsoft TV Technologies]","described","mstv.isbe2spanningevent","sbe/ISBE2SpanningEvent"]
old-location: mstv\isbe2spanningevent.htm
tech.root: mstv
ms.assetid: 155a2e61-3b53-4225-b298-ee51e2afca96
ms.date: 12/05/2018
ms.keywords: ISBE2SpanningEvent, ISBE2SpanningEvent interface [Microsoft TV Technologies], ISBE2SpanningEvent interface [Microsoft TV Technologies],described, mstv.isbe2spanningevent, sbe/ISBE2SpanningEvent
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
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
 - ISBE2SpanningEvent
 - sbe/ISBE2SpanningEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.h
api_name:
 - ISBE2SpanningEvent
---

# ISBE2SpanningEvent interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Implements in-band spanning events for the Stream Buffer Engine, version 2 (SBE2). An <i>in-band spanning event</i> is an in-band event  that can be recorded as part of the state information in a stream.

 Spanning events have a defined validity period within a Stream Buffer Interface file and may be recovered after a seek operation, updated, or deleted. Spanning events are intended for data with a defined lifespan, such as Digital Rights Management (DRM) keys or ratings information.

## -inheritance

The <b>ISBE2SpanningEvent</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISBE2SpanningEvent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

An in-band spanning event has a persisting semantic: it exists until it is replaced or erased, and it is part of the state for events that follow it in a stream. For example, the format of a stream is stored as an in-band spanning event because it can change over time. Video may consist of high definition (HD) content at the beginning of a recording but may switch to standard definition (SD) content, then back to HD content again during the course of the recording. If the user skips from SD to HD or vice versa, a dynamic format change occurs because the format has been stored as a spanning event.

In-band spanning events are also available for use by modules other than SBE2.  For example, content protection could store the protection policy as a spanning event. A recording might begin as unprotected content and then become protected midway through. An in-band spanning event indicating protected content would replace the in-band spanning event indicating protected content. As with the stream format example in the preceding paragraph, a skip from unprotected to protected content causes the in-band spanning event to be sourced.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ISBE2SpanningEvent)</code>.
