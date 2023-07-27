---
UID: NS:mpegtype.tagAM_MPEGSYSTEMTYPE
title: AM_MPEGSYSTEMTYPE (mpegtype.h)
description: The AM_MPEGSYSTEMTYPE structure defines the format block for an MPEG-1 system stream.
helpviewer_keywords: ["AM_MPEGSYSTEMTYPE","AM_MPEGSYSTEMTYPE structure [DirectShow]","dshow.am_mpegsystemtype","mpegtype/AM_MPEGSYSTEMTYPE"]
old-location: dshow\am_mpegsystemtype.htm
tech.root: dshow
ms.assetid: 218bf0c3-e618-4dcc-8618-34cd1fb5c0a8
ms.date: 4/26/2023
ms.keywords: AM_MPEGSYSTEMTYPE, AM_MPEGSYSTEMTYPE structure [DirectShow], dshow.am_mpegsystemtype, mpegtype/AM_MPEGSYSTEMTYPE
req.header: mpegtype.h
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
req.typenames: AM_MPEGSYSTEMTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAM_MPEGSYSTEMTYPE
 - mpegtype/tagAM_MPEGSYSTEMTYPE
 - AM_MPEGSYSTEMTYPE
 - mpegtype/AM_MPEGSYSTEMTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mpegtype.h
api_name:
 - AM_MPEGSYSTEMTYPE
---

# AM_MPEGSYSTEMTYPE structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AM_MPEGSYSTEMTYPE</b> structure defines the format block for an MPEG-1 system stream. This structure is used when the <b>formattype</b> member of the <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure is FORMAT_MPEG1System.

## -struct-fields

### -field dwBitRate

Bits per second.

### -field cStreams

Number of streams.

### -field Streams

List <a href="/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegstreamtype">AM_MPEGSTREAMTYPE</a> structures that describe the elementary streams. The number of elements in the list is given by the <b>cStream</b> member. The size of each <b>AM_MPEGSTREAMTYPE</b> structure is variable. Use the <b>AM_MPEGSTREAMTYPE_ELEMENTLENGTH</b> macro to calculate the size of each structure.

## -remarks

The <b>Streams</b> member contains a list of <a href="/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegstreamtype">AM_MPEGSTREAMTYPE</a> structures. The size of each <b>AM_MPEGSTREAMTYPE</b> structure is aligned to an 8-byte boundary. Given a pointer to an <b>AM_MPEGSTREAMTYPE</b> structure in list, use the <b>AM_MPEGSTREAMTYPE_NEXT</b> macro to get a pointer to the next structure.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/DirectShow/mpeg-1-media-types">MEPG-1 Media Types</a>