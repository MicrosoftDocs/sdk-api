---
UID: NS:avifmt.AVIPALCHANGE
title: AVIPALCHANGE (avifmt.h)
description: The AVIPALCHANGE structure defines a palette change in an AVI file.
helpviewer_keywords: ["AVIPALCHANGE","AVIPALCHANGE structure [DirectShow]","AVIPALCHANGEStructure","_AVIPALchange","avifmt/AVIPALCHANGE","dshow.avipalchange"]
old-location: dshow\avipalchange.htm
tech.root: dshow
ms.assetid: f8f38fe0-f506-4cf8-9a6d-381cf46b51a4
ms.date: 4/26/2023
ms.keywords: AVIPALCHANGE, AVIPALCHANGE structure [DirectShow], AVIPALCHANGEStructure, _AVIPALchange, avifmt/AVIPALCHANGE, dshow.avipalchange
req.header: avifmt.h
req.include-header: Vfw.h
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
req.typenames: AVIPALCHANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AVIPALCHANGE
 - avifmt/AVIPALCHANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - avifmt.h
api_name:
 - AVIPALCHANGE
---

# AVIPALCHANGE structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AVIPALCHANGE</b> structure defines a palette change in an AVI file.

## -struct-fields

### -field bFirstEntry

Specifies the index of the first palette entry to change.

### -field bNumEntries

Specifies the number of palette entries to change, or zero to change all 256 palette entries.

### -field wFlags

Reserved.

### -field peNew

Specifies an array of <a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a> structures, of size <b>bNumEntries</b>.

## -see-also

<a href="/windows/desktop/DirectShow/avi-riff-file-reference">AVI RIFF File Reference</a>



<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>

