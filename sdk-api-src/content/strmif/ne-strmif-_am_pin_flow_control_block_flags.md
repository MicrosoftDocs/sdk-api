---
UID: NE:strmif._AM_PIN_FLOW_CONTROL_BLOCK_FLAGS
title: "_AM_PIN_FLOW_CONTROL_BLOCK_FLAGS (strmif.h)"
description: Defines flags that specify how to block data flow from an output pin.
helpviewer_keywords: ["AM_PIN_CONNECTION_BLOCK_FLAGSEnumeration","AM_PIN_FLOW_CONTROL_BLOCK","_AM_PIN_FLOW_CONTROL_BLOCK_FLAGS","_AM_PIN_FLOW_CONTROL_BLOCK_FLAGS","_AM_PIN_FLOW_CONTROL_BLOCK_FLAGS enumeration [DirectShow]","dshow.am_pin_connection_block_flags","strmif/AM_PIN_FLOW_CONTROL_BLOCK","strmif/_AM_PIN_FLOW_CONTROL_BLOCK_FLAGS"]
old-location: dshow\am_pin_connection_block_flags.htm
tech.root: dshow
ms.assetid: ad059d7c-86dd-41a4-8cef-dbd154057c50
ms.date: 4/26/2023
ms.keywords: AM_PIN_CONNECTION_BLOCK_FLAGSEnumeration, AM_PIN_FLOW_CONTROL_BLOCK, _AM_PIN_FLOW_CONTROL_BLOCK_FLAGS, _AM_PIN_FLOW_CONTROL_BLOCK_FLAGS , _AM_PIN_FLOW_CONTROL_BLOCK_FLAGS enumeration [DirectShow], dshow.am_pin_connection_block_flags, strmif/AM_PIN_FLOW_CONTROL_BLOCK, strmif/_AM_PIN_FLOW_CONTROL_BLOCK_FLAGS
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_PIN_FLOW_CONTROL_BLOCK_FLAGS
 - strmif/_AM_PIN_FLOW_CONTROL_BLOCK_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Strmif.h
api_name:
 - _AM_PIN_FLOW_CONTROL_BLOCK_FLAGS
---

# _AM_PIN_FLOW_CONTROL_BLOCK_FLAGS enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Defines flags that specify how to block data flow from an output pin.

## -enum-fields

### -field AM_PIN_FLOW_CONTROL_BLOCK:0x1

Block the data flow.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ipinflowcontrol-block">IPinFlowControl::Block</a>
