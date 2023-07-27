---
UID: NN:strmif.IMPEG2StreamIdMap
title: IMPEG2StreamIdMap (strmif.h)
description: This interface is implemented on each output pin of the MPEG-2 Demultiplexer filter (Demux) and is used in program stream mode only.
helpviewer_keywords: ["IMPEG2StreamIdMap","IMPEG2StreamIdMap interface [DirectShow]","IMPEG2StreamIdMap interface [DirectShow]","described","IMPEG2StreamIdMapInterface","dshow.impeg2streamidmap","strmif/IMPEG2StreamIdMap"]
old-location: dshow\impeg2streamidmap.htm
tech.root: dshow
ms.assetid: 714c6b0e-3885-4026-8a83-06b37cc97d7c
ms.date: 4/26/2023
ms.keywords: IMPEG2StreamIdMap, IMPEG2StreamIdMap interface [DirectShow], IMPEG2StreamIdMap interface [DirectShow],described, IMPEG2StreamIdMapInterface, dshow.impeg2streamidmap, strmif/IMPEG2StreamIdMap
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMPEG2StreamIdMap
 - strmif/IMPEG2StreamIdMap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMPEG2StreamIdMap
---

# IMPEG2StreamIdMap interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

This interface is implemented on each output pin of the <a href="/windows/desktop/DirectShow/mpeg-2-demultiplexer">MPEG-2 Demultiplexer</a> filter (Demux) and is used in program stream mode only. It is called by applications or other filters to associate the pin with a specified Stream ID and to inform the pin whether substream filtering is required on the stream. This interface is not exposed when the filter is playing back a file (pull-mode).

For transport streams, use the <a href="/previous-versions/windows/desktop/api/bdaiface/nn-bdaiface-impeg2pidmap">IMPEG2PIDMap</a> interface.

## -inheritance

The <b>IMPEG2StreamIdMap</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMPEG2StreamIdMap</b> also has these types of members:

