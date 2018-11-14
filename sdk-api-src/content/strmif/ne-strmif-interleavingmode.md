---
UID: NE:strmif.InterleavingMode
title: InterleavingMode
author: windows-sdk-content
description: Specifies how video frames and audio samples will be written to disk.
old-location: dshow\interleavingmode.htm
tech.root: DirectShow
ms.assetid: 4011b1e4-4bcf-4a2e-9d9a-ccdc8e12cd5a
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: INTERLEAVE_CAPTURE, INTERLEAVE_FULL, INTERLEAVE_NONE, INTERLEAVE_NONE_BUFFERED, InterleavingMode, InterleavingMode enumeration [DirectShow], InterleavingModeEnumeration, dshow.interleavingmode, strmif/INTERLEAVE_CAPTURE, strmif/INTERLEAVE_FULL, strmif/INTERLEAVE_NONE, strmif/INTERLEAVE_NONE_BUFFERED, strmif/InterleavingMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - InterleavingMode
product: Windows
targetos: Windows
req.typenames: InterleavingMode
req.redist: 
---

# InterleavingMode enumeration


## -description



Specifies how video frames and audio samples will be written to disk.




## -enum-fields




### -field INTERLEAVE_NONE

Noninterleaved. Frames are written in the order they arrive. Files must be interleaved for playback at a later time. In this mode, the AVI Mux filter attempts to use unbuffered, overlapped write operations, to increase throughput.


### -field INTERLEAVE_CAPTURE

Approximate interleaving with less overhead than <b>INTERLEAVE_FULL</b>. This mode is suitable for video capture. The AVI Mux attempts to use unbuffered, overlapped write operations. Unless the interleaving parameters are configured properly, however, frames may be dropped if one stream blocks while it waits for data from another stream. In particular, audio buffers should be less than .5 second, or else the video stream will block for excessive periods of time.


### -field INTERLEAVE_FULL

Full, precise interleaving of audio samples and video frames. Streams will block indefinitely, waiting for equal amounts of data before interleaving. This mode is suitable for authoring and playback.


### -field INTERLEAVE_NONE_BUFFERED

Noninterleaved. This mode is equivalent to <b>INTERLEAVE_NONE</b> but uses less file space and system overhead.


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

