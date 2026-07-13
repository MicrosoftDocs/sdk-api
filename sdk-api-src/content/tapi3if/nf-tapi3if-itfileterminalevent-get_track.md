---
UID: NF:tapi3if.ITFileTerminalEvent.get_Track
title: ITFileTerminalEvent::get_Track (tapi3if.h)
description: The get_Track method returns the track terminal that generated this event.
helpviewer_keywords: ["ITFileTerminalEvent interface [TAPI 2.2]","get_Track method","ITFileTerminalEvent.get_Track","ITFileTerminalEvent::get_Track","_tapi3_itfileterminalevent_get_track","get_Track","get_Track method [TAPI 2.2]","get_Track method [TAPI 2.2]","ITFileTerminalEvent interface","tapi3.itfileterminalevent_get_track","tapi3if/ITFileTerminalEvent::get_Track"]
old-location: tapi3\itfileterminalevent_get_track.htm
tech.root: tapi3
ms.assetid: f860faf3-6ca5-43d3-8d68-487d1b1d29b0
ms.date: 12/05/2018
ms.keywords: ITFileTerminalEvent interface [TAPI 2.2],get_Track method, ITFileTerminalEvent.get_Track, ITFileTerminalEvent::get_Track, _tapi3_itfileterminalevent_get_track, get_Track, get_Track method [TAPI 2.2], get_Track method [TAPI 2.2],ITFileTerminalEvent interface, tapi3.itfileterminalevent_get_track, tapi3if/ITFileTerminalEvent::get_Track
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
 - ITFileTerminalEvent::get_Track
 - tapi3if/ITFileTerminalEvent::get_Track
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
 - ITFileTerminalEvent.get_Track
---

# ITFileTerminalEvent::get_Track


## -description

The 
<b>get_Track</b> method returns the track terminal that generated this event.

## -parameters

### -param ppTrackTerminal [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack">ITFileTrack</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itfileterminalevent">ITFileTerminalEvent</a>