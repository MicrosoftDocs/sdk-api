---
UID: NF:sbe.ISBE2GlobalEvent.GetEvent
title: ISBE2GlobalEvent::GetEvent (sbe.h)
description: Gets a global spanning event and its data from a Stream Buffer Source filter.
helpviewer_keywords: ["GetEvent","GetEvent method [Microsoft TV Technologies]","GetEvent method [Microsoft TV Technologies]","ISBE2GlobalEvent interface","ISBE2GlobalEvent interface [Microsoft TV Technologies]","GetEvent method","ISBE2GlobalEvent.GetEvent","ISBE2GlobalEvent::GetEvent","mstv.isbe2globalevent_getevent","sbe/ISBE2GlobalEvent::GetEvent"]
old-location: mstv\isbe2globalevent_getevent.htm
tech.root: mstv
ms.assetid: 2ffa323d-6793-49e2-98ea-b9349c946c7c
ms.date: 12/05/2018
ms.keywords: GetEvent, GetEvent method [Microsoft TV Technologies], GetEvent method [Microsoft TV Technologies],ISBE2GlobalEvent interface, ISBE2GlobalEvent interface [Microsoft TV Technologies],GetEvent method, ISBE2GlobalEvent.GetEvent, ISBE2GlobalEvent::GetEvent, mstv.isbe2globalevent_getevent, sbe/ISBE2GlobalEvent::GetEvent
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
 - ISBE2GlobalEvent::GetEvent
 - sbe/ISBE2GlobalEvent::GetEvent
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
 - ISBE2GlobalEvent.GetEvent
---

# ISBE2GlobalEvent::GetEvent


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a global spanning event and its data from a <a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter.

## -parameters

### -param idEvt [in]

GUID identifying the event.

### -param param1 [in]

First event-specific parameter.

### -param param2 [in]

Second event-specific parameter.

### -param param3 [in]

Third  event-specific parameter.

### -param param4 [in]

Fourth  event-specific parameter.

### -param pSpanning [out]

Receives a flag indicating whether the event is a spanning event.

### -param pcb [in, out]

Pointer to a value specifying the buffer size. If the <i>pb</i> parameter is <b>NULL</b>, this parameter returns the required buffer size.

### -param pb [out]

Pointer to a buffer that receives the event data. If this parameter is <b>NULL</b>, the <i>pcb</i> parameter returns the required buffer size. The structure of the event data depends on the event type. For a list of event types, see the description of the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2spanningevent-getevent">ISBE2SpanningEvent::GetEvent</a> method.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following:

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_INSUFFICIENT_BUFFER</dt>
</dl>
</td>
<td width="60%">
Buffer was too small to hold event data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ERROR_CONTEXT_EXPIRED</dt>
</dl>
</td>
<td width="60%">
Too much time elapsed between the broadcast event and the call to retrieve it.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2globalevent">ISBE2GlobalEvent</a>



<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2spanningevent-getevent">ISBE2SpanningEvent::GetEvent</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source Filter</a>