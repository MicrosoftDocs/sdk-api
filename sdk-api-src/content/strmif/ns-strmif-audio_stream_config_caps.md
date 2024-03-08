---
UID: NS:strmif._AUDIO_STREAM_CONFIG_CAPS
title: AUDIO_STREAM_CONFIG_CAPS (strmif.h)
description: The AUDIO_STREAM_CONFIG_CAPS structure describes a range of audio formats. Audio compression and capture filters use this structure to describe the formats they can produce.
helpviewer_keywords: ["AUDIO_STREAM_CONFIG_CAPS","AUDIO_STREAM_CONFIG_CAPS structure [DirectShow]","AUDIO_STREAM_CONFIG_CAPSStructure","dshow.audio_stream_config_caps","strmif/AUDIO_STREAM_CONFIG_CAPS"]
old-location: dshow\audio_stream_config_caps.htm
tech.root: dshow
ms.assetid: 8a923e8e-173e-4258-ba81-7d398bd9c5fe
ms.date: 4/26/2023
ms.keywords: AUDIO_STREAM_CONFIG_CAPS, AUDIO_STREAM_CONFIG_CAPS structure [DirectShow], AUDIO_STREAM_CONFIG_CAPSStructure, dshow.audio_stream_config_caps, strmif/AUDIO_STREAM_CONFIG_CAPS
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
req.typenames: AUDIO_STREAM_CONFIG_CAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AUDIO_STREAM_CONFIG_CAPS
 - strmif/_AUDIO_STREAM_CONFIG_CAPS
 - AUDIO_STREAM_CONFIG_CAPS
 - strmif/AUDIO_STREAM_CONFIG_CAPS
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
 - AUDIO_STREAM_CONFIG_CAPS
---

# AUDIO_STREAM_CONFIG_CAPS structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AUDIO_STREAM_CONFIG_CAPS</b> structure describes a range of audio formats. Audio compression and capture filters use this structure to describe the formats they can produce.

## -struct-fields

### -field guid

Will be set to MEDIATYPE_Audio to indicate an audio sample.

### -field MinimumChannels

Minimum number of channels.

### -field MaximumChannels

Maximum number of channels.

### -field ChannelsGranularity

Granularity of the channels. For example, the filter might specify channels 2 through 4, in steps of 2.

### -field MinimumBitsPerSample

Minimum bits per sample.

### -field MaximumBitsPerSample

Maximum bits per sample.

### -field BitsPerSampleGranularity

Granularity of the bits per sample. For example, the filter might specify 8 bits per sample through 32 bits per sample, in steps of 8.

### -field MinimumSampleFrequency

Minimum sample frequency.

### -field MaximumSampleFrequency

Maximum sample frequency.

### -field SampleFrequencyGranularity

Granularity of the frequency. For example, the filter might specify 11025 Hz to 44100 Hz, in steps of 11025 Hz.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamstreamconfig-getstreamcaps">IAMStreamConfig::GetStreamCaps</a>