---
UID: NF:strmif.IMPEG2StreamIdMap.MapStreamId
title: IMPEG2StreamIdMap::MapStreamId (strmif.h)
description: The MapStreamId method maps the Stream ID of an elementary stream within an MPEG-2 program stream to a media content type and substream filtering information.
helpviewer_keywords: ["IMPEG2StreamIdMap interface [DirectShow]","MapStreamId method","IMPEG2StreamIdMap.MapStreamId","IMPEG2StreamIdMap::MapStreamId","IMPEG2StreamIdMapMapStreamId","MapStreamId","MapStreamId method [DirectShow]","MapStreamId method [DirectShow]","IMPEG2StreamIdMap interface","dshow.impeg2streamidmap_mapstreamid","strmif/IMPEG2StreamIdMap::MapStreamId"]
old-location: dshow\impeg2streamidmap_mapstreamid.htm
tech.root: dshow
ms.assetid: e74a1e62-1bc4-43e1-9017-85012b2ece01
ms.date: 4/26/2023
ms.keywords: IMPEG2StreamIdMap interface [DirectShow],MapStreamId method, IMPEG2StreamIdMap.MapStreamId, IMPEG2StreamIdMap::MapStreamId, IMPEG2StreamIdMapMapStreamId, MapStreamId, MapStreamId method [DirectShow], MapStreamId method [DirectShow],IMPEG2StreamIdMap interface, dshow.impeg2streamidmap_mapstreamid, strmif/IMPEG2StreamIdMap::MapStreamId
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
 - IMPEG2StreamIdMap::MapStreamId
 - strmif/IMPEG2StreamIdMap::MapStreamId
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
 - IMPEG2StreamIdMap.MapStreamId
---

# IMPEG2StreamIdMap::MapStreamId


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>MapStreamId</code> method maps the Stream ID of an elementary stream within an MPEG-2 program stream to a media content type and substream filtering information.

## -parameters

### -param ulStreamId [in]

The stream ID of the PES stream.

### -param MediaSampleContent [in]

Specifies the contents of the stream. Currently the only value supported is MPEG2_PROGRAM_ELEMENTARY_STREAM (defined as 0x00000001 in axextend.idl).

### -param ulSubstreamFilterValue [in]

Specifies which substream within this elementary stream to pass on to the downstream decoder. Only the low-order byte can contain a valid filter value. If <i>iDataOffset</i> = 0, this parameter is ignored.

### -param iDataOffset [in]

The byte offset into the payload at which the substream begins.

## -returns

Returns S_OK if successful. If the method fails, an error code is returned. If a Stream ID of MEDIA_PROGRAM_STREAM_MAP, MEDIA_PROGRAM_DIRECTORY_PES_PACKET or MEDIA_PROGRAM_PACK_HEADER is attempted, this method returns E_NOTIMPL.

## -remarks

The Stream ID mapped by this method is the stream ID in the PES header. Substream filtering is most commonly used to provide multiple channels on a single audio stream.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-impeg2streamidmap">IMPEG2StreamIdMap Interface</a>