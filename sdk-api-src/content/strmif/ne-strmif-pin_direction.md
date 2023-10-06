---
UID: NE:strmif._PinDirection
title: PIN_DIRECTION (strmif.h)
description: Indicates a pin's direction.
helpviewer_keywords: ["PINDIR_INPUT","PINDIR_OUTPUT","PIN_DIRECTION","PIN_DIRECTION","PIN_DIRECTION enumeration [DirectShow]","PIN_DIRECTIONEnumeration","dshow.pin_direction","strmif/PINDIR_INPUT","strmif/PINDIR_OUTPUT","strmif/PIN_DIRECTION"]
old-location: dshow\pin_direction.htm
tech.root: dshow
ms.assetid: 87f4e2e8-543f-46a3-b385-cc2e6af39770
ms.date: 4/26/2023
ms.keywords: PINDIR_INPUT, PINDIR_OUTPUT, PIN_DIRECTION, PIN_DIRECTION , PIN_DIRECTION enumeration [DirectShow], PIN_DIRECTIONEnumeration, dshow.pin_direction, strmif/PINDIR_INPUT, strmif/PINDIR_OUTPUT, strmif/PIN_DIRECTION
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
req.typenames: PIN_DIRECTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PinDirection
 - strmif/_PinDirection
 - PIN_DIRECTION
 - strmif/PIN_DIRECTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - PIN_DIRECTION
---

# PIN_DIRECTION enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Indicates a pin's direction.

## -enum-fields

### -field PINDIR_INPUT:0

Input pin.

### -field PINDIR_OUTPUT

Output pin.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ipin-querydirection">IPin::QueryDirection</a>
