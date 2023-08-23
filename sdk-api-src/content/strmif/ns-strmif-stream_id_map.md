---
UID: NS:strmif.STREAM_ID_MAP
title: STREAM_ID_MAP (strmif.h)
description: The STREAM_ID_MAP structure describes an elementary stream within an MPEG-2 program stream. Used with the IEnumStreamIdMap interface methods.
helpviewer_keywords: ["MPEG2_PROGRAM_DIRECTORY_PES_PACKET","MPEG2_PROGRAM_ELEMENTARY_STREAM","MPEG2_PROGRAM_PACK_HEADER","MPEG2_PROGRAM_PES_STREAM","MPEG2_PROGRAM_STREAM_MAP","MPEG2_PROGRAM_SYSTEM_HEADER","STREAM_ID_MAP","STREAM_ID_MAP structure [DirectShow]","STREAM_ID_MAPStructure","dshow.stream_id_map","strmif/STREAM_ID_MAP"]
old-location: dshow\stream_id_map.htm
tech.root: dshow
ms.assetid: 75f41d9f-00a1-47e1-8b42-64de1e6abbdb
ms.date: 4/26/2023
ms.keywords: MPEG2_PROGRAM_DIRECTORY_PES_PACKET, MPEG2_PROGRAM_ELEMENTARY_STREAM, MPEG2_PROGRAM_PACK_HEADER, MPEG2_PROGRAM_PES_STREAM, MPEG2_PROGRAM_STREAM_MAP, MPEG2_PROGRAM_SYSTEM_HEADER, STREAM_ID_MAP, STREAM_ID_MAP structure [DirectShow], STREAM_ID_MAPStructure, dshow.stream_id_map, strmif/STREAM_ID_MAP
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
req.typenames: STREAM_ID_MAP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - STREAM_ID_MAP
 - strmif/STREAM_ID_MAP
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
 - STREAM_ID_MAP
---

# STREAM_ID_MAP structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>STREAM_ID_MAP</code> structure describes an elementary stream within an MPEG-2 program stream. Used with the <a href="/windows/desktop/api/strmif/nn-strmif-ienumstreamidmap">IEnumStreamIdMap</a> interface methods.

## -struct-fields

### -field stream_id

Specifies the ID of the PES stream.

### -field dwMediaSampleContent

Specifies the media contents of the stream. May be one of the following values defined in axextend.idl:



#### MPEG2_PROGRAM_STREAM_MAP (0x00000000)



#### MPEG2_PROGRAM_ELEMENTARY_STREAM (0x00000001)



#### MPEG2_PROGRAM_DIRECTORY_PES_PACKET (0x00000002)



#### MPEG2_PROGRAM_PACK_HEADER (0x00000003)



#### MPEG2_PROGRAM_PES_STREAM (0x00000004)



#### MPEG2_PROGRAM_SYSTEM_HEADER (0x00000005)

### -field ulSubstreamFilterValue

Specifies the substream within the elementary stream. If no substream filtering is required, use SUBSTREAM_FILTER_VAL_NONE (0x10000000).

### -field iDataOffset

Specifies the offset in bytes for the substream. If no filtering is required, specify 0.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>