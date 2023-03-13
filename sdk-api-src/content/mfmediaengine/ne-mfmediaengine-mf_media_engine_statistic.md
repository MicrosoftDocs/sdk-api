---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_STATISTIC
title: MF_MEDIA_ENGINE_STATISTIC (mfmediaengine.h)
description: Identifies statistics that the Media Engine tracks during playback.
helpviewer_keywords: ["MF_MEDIA_ENGINE_STATISTIC","MF_MEDIA_ENGINE_STATISTIC enumeration [Media Foundation]","MF_MEDIA_ENGINE_STATISTIC_BUFFER_PROGRESS","MF_MEDIA_ENGINE_STATISTIC_BYTES_DOWNLOADED","MF_MEDIA_ENGINE_STATISTIC_FRAMES_CORRUPTED","MF_MEDIA_ENGINE_STATISTIC_FRAMES_DROPPED","MF_MEDIA_ENGINE_STATISTIC_FRAMES_PER_SECOND","MF_MEDIA_ENGINE_STATISTIC_FRAMES_RENDERED","MF_MEDIA_ENGINE_STATISTIC_PLAYBACK_JITTER","MF_MEDIA_ENGINE_STATISTIC_TOTAL_FRAME_DELAY","mf.mf_media_engine_statistic","mfmediaengine/ MF_MEDIA_ENGINE_STATISTIC_FRAMES_CORRUPTED","mfmediaengine/ MF_MEDIA_ENGINE_STATISTIC_PLAYBACK_JITTER","mfmediaengine/ MF_MEDIA_ENGINE_STATISTIC_TOTAL_FRAME_DELAY","mfmediaengine/MF_MEDIA_ENGINE_STATISTIC","mfmediaengine/MF_MEDIA_ENGINE_STATISTIC_BUFFER_PROGRESS","mfmediaengine/MF_MEDIA_ENGINE_STATISTIC_BYTES_DOWNLOADED","mfmediaengine/MF_MEDIA_ENGINE_STATISTIC_FRAMES_DROPPED","mfmediaengine/MF_MEDIA_ENGINE_STATISTIC_FRAMES_PER_SECOND","mfmediaengine/MF_MEDIA_ENGINE_STATISTIC_FRAMES_RENDERED"]
old-location: mf\mf_media_engine_statistic.htm
tech.root: mf
ms.assetid: EB431C2F-69A3-4376-BEC7-A5AE0329AD15
ms.date: 12/05/2018
ms.keywords: MF_MEDIA_ENGINE_STATISTIC, MF_MEDIA_ENGINE_STATISTIC enumeration [Media Foundation], MF_MEDIA_ENGINE_STATISTIC_BUFFER_PROGRESS, MF_MEDIA_ENGINE_STATISTIC_BYTES_DOWNLOADED, MF_MEDIA_ENGINE_STATISTIC_FRAMES_CORRUPTED, MF_MEDIA_ENGINE_STATISTIC_FRAMES_DROPPED, MF_MEDIA_ENGINE_STATISTIC_FRAMES_PER_SECOND, MF_MEDIA_ENGINE_STATISTIC_FRAMES_RENDERED, MF_MEDIA_ENGINE_STATISTIC_PLAYBACK_JITTER, MF_MEDIA_ENGINE_STATISTIC_TOTAL_FRAME_DELAY, mf.mf_media_engine_statistic, mfmediaengine/ MF_MEDIA_ENGINE_STATISTIC_FRAMES_CORRUPTED, mfmediaengine/ MF_MEDIA_ENGINE_STATISTIC_PLAYBACK_JITTER, mfmediaengine/ MF_MEDIA_ENGINE_STATISTIC_TOTAL_FRAME_DELAY, mfmediaengine/MF_MEDIA_ENGINE_STATISTIC, mfmediaengine/MF_MEDIA_ENGINE_STATISTIC_BUFFER_PROGRESS, mfmediaengine/MF_MEDIA_ENGINE_STATISTIC_BYTES_DOWNLOADED, mfmediaengine/MF_MEDIA_ENGINE_STATISTIC_FRAMES_DROPPED, mfmediaengine/MF_MEDIA_ENGINE_STATISTIC_FRAMES_PER_SECOND, mfmediaengine/MF_MEDIA_ENGINE_STATISTIC_FRAMES_RENDERED
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: MF_MEDIA_ENGINE_STATISTIC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MF_MEDIA_ENGINE_STATISTIC
 - mfmediaengine/MF_MEDIA_ENGINE_STATISTIC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfmediaengine.h
api_name:
 - MF_MEDIA_ENGINE_STATISTIC
---

# MF_MEDIA_ENGINE_STATISTIC enumeration


## -description

Identifies statistics that the Media Engine tracks during playback. To get a playback statistic from the Media Engine, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getstatistics">IMFMediaEngineEx::GetStatistics</a>.

In the descriptions that follow, the data type and value-type tag for the <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> are listed in parentheses.

## -enum-fields

### -field MF_MEDIA_ENGINE_STATISTIC_FRAMES_RENDERED:0

The number of rendered video frames. (<b>ULONG</b>, <b>VT_UI4</b>)

### -field MF_MEDIA_ENGINE_STATISTIC_FRAMES_DROPPED:1

The number of dropped video frames. (<b>ULONG</b>, <b>VT_UI4</b>)

### -field MF_MEDIA_ENGINE_STATISTIC_BYTES_DOWNLOADED:2

The number of bytes that have been downloaded since the last HTTP range request. (<b>ULARGE_INTEGER</b>, <b>VT_UI8</b>).

### -field MF_MEDIA_ENGINE_STATISTIC_BUFFER_PROGRESS:3

The percentage of the playout buffer filled during buffering. The value is an integer in the range 0–100. (<b>LONG</b>, <b>VT_I4</b>)

### -field MF_MEDIA_ENGINE_STATISTIC_FRAMES_PER_SECOND:4

The frames per second. (<b>FLOAT</b>, <b>VT_R4</b>)

### -field MF_MEDIA_ENGINE_STATISTIC_PLAYBACK_JITTER:5

The amount of playback jitter. (<b>DOUBLE</b>, <b>VT_R8</b>)

Supported in Windows 8.1 and later.

### -field MF_MEDIA_ENGINE_STATISTIC_FRAMES_CORRUPTED:6

The number of corrupted frames. (<b>ULONG</b>, <b>VT_UI4</b>)

Supported in Windows 8.1 and later.

### -field MF_MEDIA_ENGINE_STATISTIC_TOTAL_FRAME_DELAY:7

The total amount of frame delay.  (<b>DOUBLE</b>, <b>VT_R8</b>)

Supported in Windows 8.1 and later.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getstatistics">IMFMediaEngineEx::GetStatistics</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
