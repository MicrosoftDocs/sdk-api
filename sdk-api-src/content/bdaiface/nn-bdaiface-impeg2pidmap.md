---
UID: NN:bdaiface.IMPEG2PIDMap
title: IMPEG2PIDMap (bdaiface.h)
description: This interface is implemented on each output pin of the MPEG-2 Demultiplexer filter (Demux) and is used in transport stream mode only.
helpviewer_keywords: ["IMPEG2PIDMap","IMPEG2PIDMap interface [DirectShow]","IMPEG2PIDMap interface [DirectShow]","described","IMPEG2PIDMapInterface","bdaiface/IMPEG2PIDMap","dshow.impeg2pidmap"]
old-location: dshow\impeg2pidmap.htm
tech.root: dshow
ms.assetid: 45c09a02-7da8-460a-9a64-f012c2181b94
ms.date: 4/26/2023
ms.keywords: IMPEG2PIDMap, IMPEG2PIDMap interface [DirectShow], IMPEG2PIDMap interface [DirectShow],described, IMPEG2PIDMapInterface, bdaiface/IMPEG2PIDMap, dshow.impeg2pidmap
req.header: bdaiface.h
req.include-header: 
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
 - IMPEG2PIDMap
 - bdaiface/IMPEG2PIDMap
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
 - IMPEG2PIDMap
---

# IMPEG2PIDMap interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

This interface is implemented on each output pin of the <a href="/windows/desktop/DirectShow/mpeg-2-demultiplexer">MPEG-2 Demultiplexer</a> filter (Demux) and is used in transport stream mode only. It is called by applications or other filters to associate the pin with one or more Packet IDs (PID). Once a PID has been mapped, the Demux will deliver all packets with that ID to the output pin. This interface is not exposed when the filter is playing back a file (pull-mode).

For program streams, use the <a href="/windows/desktop/api/strmif/nn-strmif-impeg2streamidmap">IMPEG2StreamIdMap</a> interface.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="/previous-versions/windows/desktop/mstv/ocur-devices">OCUR Devices</a>.

## -inheritance

The <b>IMPEG2PIDMap</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMPEG2PIDMap</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
