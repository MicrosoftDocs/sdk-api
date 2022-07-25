---
UID: NF:tapi3if.ITMediaControl.get_MediaState
title: ITMediaControl::get_MediaState (tapi3if.h)
description: The get_MediaState method gets the current state of media on the file terminal.
helpviewer_keywords: ["ITMediaControl interface [TAPI 2.2]","get_MediaState method","ITMediaControl.get_MediaState","ITMediaControl::get_MediaState","_tapi3_itmediacontrol_get_mediastate","get_MediaState","get_MediaState method [TAPI 2.2]","get_MediaState method [TAPI 2.2]","ITMediaControl interface","tapi3.itmediacontrol_get_mediastate","tapi3if/ITMediaControl::get_MediaState"]
old-location: tapi3\itmediacontrol_get_mediastate.htm
tech.root: tapi3
ms.assetid: d28063cc-12fe-45b1-8f6a-8c2436926e12
ms.date: 12/05/2018
ms.keywords: ITMediaControl interface [TAPI 2.2],get_MediaState method, ITMediaControl.get_MediaState, ITMediaControl::get_MediaState, _tapi3_itmediacontrol_get_mediastate, get_MediaState, get_MediaState method [TAPI 2.2], get_MediaState method [TAPI 2.2],ITMediaControl interface, tapi3.itmediacontrol_get_mediastate, tapi3if/ITMediaControl::get_MediaState
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
 - ITMediaControl::get_MediaState
 - tapi3if/ITMediaControl::get_MediaState
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
 - ITMediaControl.get_MediaState
---

# ITMediaControl::get_MediaState


## -description

The 
<b>get_MediaState</b> method gets the current state of media on the file terminal.

## -parameters

### -param pTerminalMediaState [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_media_state">TERMINAL_MEDIA_STATE</a> descriptor of the current state of the file terminal.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol">ITMediaControl</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_media_state">TERMINAL_MEDIA_STATE</a>