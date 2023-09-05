---
UID: NF:sbe.ISBE2GlobalEvent2.GetEventEx
title: ISBE2GlobalEvent2::GetEventEx (sbe.h)
description: Gets a global spanning event and its data from a Stream Buffer Source filter.
helpviewer_keywords: ["GetEventEx","GetEventEx method [Microsoft TV Technologies]","GetEventEx method [Microsoft TV Technologies]","ISBE2GlobalEvent2 interface","ISBE2GlobalEvent2 interface [Microsoft TV Technologies]","GetEventEx method","ISBE2GlobalEvent2.GetEventEx","ISBE2GlobalEvent2::GetEventEx","mstv.isbe2globalevent2_geteventex","sbe/ISBE2GlobalEvent2::GetEventEx"]
old-location: mstv\isbe2globalevent2_geteventex.htm
tech.root: mstv
ms.assetid: 44c30d8a-d62b-4e0f-8ff9-a4159df6d724
ms.date: 12/05/2018
ms.keywords: GetEventEx, GetEventEx method [Microsoft TV Technologies], GetEventEx method [Microsoft TV Technologies],ISBE2GlobalEvent2 interface, ISBE2GlobalEvent2 interface [Microsoft TV Technologies],GetEventEx method, ISBE2GlobalEvent2.GetEventEx, ISBE2GlobalEvent2::GetEventEx, mstv.isbe2globalevent2_geteventex, sbe/ISBE2GlobalEvent2::GetEventEx
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
 - ISBE2GlobalEvent2::GetEventEx
 - sbe/ISBE2GlobalEvent2::GetEventEx
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
 - ISBE2GlobalEvent2.GetEventEx
---

# ISBE2GlobalEvent2::GetEventEx


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

Third event-specific parameter.

### -param param4 [in]

Fourth event-specific parameter.

### -param pSpanning [out]

Receives a flag indicating whether the event is a spanning event.

### -param pcb [in, out]

Pointer to a value specifying the buffer size. If the <i>pb</i> parameter is <b>NULL</b>, this parameter returns the required buffer size.

### -param pb [out]

Pointer to a buffer that receives the event data. If this parameter is <b>NULL</b>, the <i>pcb</i> parameter returns the required buffer size. The structure of the event data depends on the event type. For a list of event types, see the description of the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2spanningevent-getevent">ISBE2SpanningEvent::GetEvent</a> method.

### -param pStreamTime [out]

Stream time of last data sample that was read from the 
    file before the event.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2globalevent2">ISBE2GlobalEvent2</a>



<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2spanningevent-getevent">ISBE2SpanningEvent::GetEvent</a>