---
UID: NF:tapi3if.ITMultiTrackTerminal.get_DirectionsInUse
title: ITMultiTrackTerminal::get_DirectionsInUse (tapi3if.h)
description: The get_DirectionsInUse method returns the direction of all tracks managed currently by the multitrack terminal.
helpviewer_keywords: ["ITMultiTrackTerminal interface [TAPI 2.2]","get_DirectionsInUse method","ITMultiTrackTerminal.get_DirectionsInUse","ITMultiTrackTerminal::get_DirectionsInUse","_tapi3_itmultitrackterminal_get_directionsinuse","get_DirectionsInUse","get_DirectionsInUse method [TAPI 2.2]","get_DirectionsInUse method [TAPI 2.2]","ITMultiTrackTerminal interface","tapi3.itmultitrackterminal_get_directionsinuse","tapi3if/ITMultiTrackTerminal::get_DirectionsInUse"]
old-location: tapi3\itmultitrackterminal_get_directionsinuse.htm
tech.root: tapi3
ms.assetid: d9f739ea-3df5-4275-868a-3e0d611254c0
ms.date: 12/05/2018
ms.keywords: ITMultiTrackTerminal interface [TAPI 2.2],get_DirectionsInUse method, ITMultiTrackTerminal.get_DirectionsInUse, ITMultiTrackTerminal::get_DirectionsInUse, _tapi3_itmultitrackterminal_get_directionsinuse, get_DirectionsInUse, get_DirectionsInUse method [TAPI 2.2], get_DirectionsInUse method [TAPI 2.2],ITMultiTrackTerminal interface, tapi3.itmultitrackterminal_get_directionsinuse, tapi3if/ITMultiTrackTerminal::get_DirectionsInUse
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
 - ITMultiTrackTerminal::get_DirectionsInUse
 - tapi3if/ITMultiTrackTerminal::get_DirectionsInUse
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
 - ITMultiTrackTerminal.get_DirectionsInUse
---

# ITMultiTrackTerminal::get_DirectionsInUse


## -description

The 
<b>get_DirectionsInUse</b> method returns the direction of all tracks managed currently by the multitrack terminal. For tracks that are multitrack terminals themselves, this method calls the track's <b>ITMultiTrackTerminal::get_DirectionsInUse</b> method to determine the track's directions.

## -parameters

### -param plDirectionsInUsed [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">TERMINAL_DIRECTION</a> descriptor of the directions.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal">ITMultiTrackTerminal</a>