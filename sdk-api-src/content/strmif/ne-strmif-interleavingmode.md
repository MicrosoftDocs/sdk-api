---
UID: NE:strmif.InterleavingMode
title: InterleavingMode (strmif.h)
description: Specifies how video frames and audio samples will be written to disk.
helpviewer_keywords: ["INTERLEAVE_CAPTURE","INTERLEAVE_FULL","INTERLEAVE_NONE","INTERLEAVE_NONE_BUFFERED","InterleavingMode","InterleavingMode enumeration [DirectShow]","InterleavingModeEnumeration","dshow.interleavingmode","strmif/INTERLEAVE_CAPTURE","strmif/INTERLEAVE_FULL","strmif/INTERLEAVE_NONE","strmif/INTERLEAVE_NONE_BUFFERED","strmif/InterleavingMode"]
old-location: dshow\interleavingmode.htm
tech.root: dshow
ms.assetid: 4011b1e4-4bcf-4a2e-9d9a-ccdc8e12cd5a
ms.date: 12/05/2018
ms.keywords: INTERLEAVE_CAPTURE, INTERLEAVE_FULL, INTERLEAVE_NONE, INTERLEAVE_NONE_BUFFERED, InterleavingMode, InterleavingMode enumeration [DirectShow], InterleavingModeEnumeration, dshow.interleavingmode, strmif/INTERLEAVE_CAPTURE, strmif/INTERLEAVE_FULL, strmif/INTERLEAVE_NONE, strmif/INTERLEAVE_NONE_BUFFERED, strmif/InterleavingMode
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
req.typenames: InterleavingMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InterleavingMode
 - strmif/InterleavingMode
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
 - InterleavingMode
---

# InterleavingMode enumeration


## -description

Specifies how video frames and audio samples will be written to disk.

## -enum-fields

### -field INTERLEAVE_NONE:0

Noninterleaved. Frames are written in the order they arrive. Files must be interleaved for playback at a later time. In this mode, the AVI Mux filter attempts to use unbuffered, overlapped write operations, to increase throughput.

### -field INTERLEAVE_CAPTURE

Approximate interleaving with less overhead than <b>INTERLEAVE_FULL</b>. This mode is suitable for video capture. The AVI Mux attempts to use unbuffered, overlapped write operations. Unless the interleaving parameters are configured properly, however, frames may be dropped if one stream blocks while it waits for data from another stream. In particular, audio buffers should be less than .5 second, or else the video stream will block for excessive periods of time.

### -field INTERLEAVE_FULL

Full, precise interleaving of audio samples and video frames. Streams will block indefinitely, waiting for equal amounts of data before interleaving. This mode is suitable for authoring and playback.

### -field INTERLEAVE_NONE_BUFFERED

Noninterleaved. This mode is equivalent to <b>INTERLEAVE_NONE</b> but uses less file space and system overhead.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
