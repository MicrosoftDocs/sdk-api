---
UID: NF:strmif.IMPEG2StreamIdMap.UnmapStreamId
title: IMPEG2StreamIdMap::UnmapStreamId (strmif.h)
description: The UnmapStreamId method unmaps the Stream ID mapping created in a previous call to MapStreamId.
helpviewer_keywords: ["IMPEG2StreamIdMap interface [DirectShow]","UnmapStreamId method","IMPEG2StreamIdMap.UnmapStreamId","IMPEG2StreamIdMap::UnmapStreamId","IMPEG2StreamIdMapUnmapStreamId","UnmapStreamId","UnmapStreamId method [DirectShow]","UnmapStreamId method [DirectShow]","IMPEG2StreamIdMap interface","dshow.impeg2streamidmap_unmapstreamid","strmif/IMPEG2StreamIdMap::UnmapStreamId"]
old-location: dshow\impeg2streamidmap_unmapstreamid.htm
tech.root: dshow
ms.assetid: 99e28b85-effd-4f86-b2da-ec02a05dde40
ms.date: 4/26/2023
ms.keywords: IMPEG2StreamIdMap interface [DirectShow],UnmapStreamId method, IMPEG2StreamIdMap.UnmapStreamId, IMPEG2StreamIdMap::UnmapStreamId, IMPEG2StreamIdMapUnmapStreamId, UnmapStreamId, UnmapStreamId method [DirectShow], UnmapStreamId method [DirectShow],IMPEG2StreamIdMap interface, dshow.impeg2streamidmap_unmapstreamid, strmif/IMPEG2StreamIdMap::UnmapStreamId
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
 - IMPEG2StreamIdMap::UnmapStreamId
 - strmif/IMPEG2StreamIdMap::UnmapStreamId
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
 - IMPEG2StreamIdMap.UnmapStreamId
---

# IMPEG2StreamIdMap::UnmapStreamId


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>UnmapStreamId</code> method unmaps the Stream ID mapping created in a previous call to <b>MapStreamId</b>.

## -parameters

### -param culStreamId [in]

The number of elements in the <i>pulStreamID</i> array.

### -param pulStreamId [in]

Array of Stream IDs mapped for this pin.

## -returns

Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.

## -remarks

There is typically only one stream ID mapped to a given pin, therefore <i>pulStreamID</i> will typically contain a single element.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-impeg2streamidmap">IMPEG2StreamIdMap Interface</a>