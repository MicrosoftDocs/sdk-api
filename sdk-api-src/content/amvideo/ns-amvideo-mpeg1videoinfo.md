---
UID: NS:amvideo.tagMPEG1VIDEOINFO
title: MPEG1VIDEOINFO (amvideo.h)
description: The MPEG1VIDEOINFO structure describes an MPEG-1 video stream.
helpviewer_keywords: ["MPEG1VIDEOINFO","MPEG1VIDEOINFO structure [DirectShow]","MPEG1VIDEOINFOStructure","amvideo/MPEG1VIDEOINFO","dshow.mpeg1videoinfo","tagMPEG1VIDEOINFO"]
old-location: dshow\mpeg1videoinfo.htm
tech.root: dshow
ms.assetid: ae5b8825-7c1c-4a44-b665-098732e6c3bc
ms.date: 4/26/2023
ms.keywords: MPEG1VIDEOINFO, MPEG1VIDEOINFO structure [DirectShow], MPEG1VIDEOINFOStructure, amvideo/MPEG1VIDEOINFO, dshow.mpeg1videoinfo, tagMPEG1VIDEOINFO
req.header: amvideo.h
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
req.typenames: MPEG1VIDEOINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMPEG1VIDEOINFO
 - amvideo/tagMPEG1VIDEOINFO
 - MPEG1VIDEOINFO
 - amvideo/MPEG1VIDEOINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - amvideo.h
api_name:
 - MPEG1VIDEOINFO
---

# MPEG1VIDEOINFO structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>MPEG1VIDEOINFO</b> structure describes an MPEG-1 video stream.

## -struct-fields

### -field hdr

<a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> structure.

### -field dwStartTimeCode

25-bit group-of-pictures (GOP) time code at start of data.

### -field cbSequenceHeader

Length of the <b>bSequenceHeader</b> member, in bytes.

### -field bSequenceHeader

Start of an array that contains the sequence header, including quantization matrices, if any. The size of the array is given in the <b>cbSequenceHeader</b> member.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>