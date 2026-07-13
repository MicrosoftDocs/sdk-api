---
UID: NF:spatialaudioclient.ISpatialAudioClient2.GetMaxFrameCountForCategory
tech.root: CoreAudio
title: ISpatialAudioClient2::GetMaxFrameCountForCategory
ms.date: 01/31/2022
targetos: Windows
description: Gets the maximum supported frame count per processing pass. 
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: spatialaudioclient.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - ISpatialAudioClient2::GetMaxFrameCountForCategory
f1_keywords:
 - ISpatialAudioClient2::GetMaxFrameCountForCategory
 - spatialaudioclient/ISpatialAudioClient2::GetMaxFrameCountForCategory
dev_langs:
 - c++
---

## -description

Gets the maximum supported frame count per processing pass. 

## -parameters

### -param category [in]

The <xref:NE:audiosessiontypes._AUDIO_STREAM_CATEGORY> of the audio stream for which support is queried.

### -param offloadEnabled [in]

A boolean value specifying whether the returned frame count should be calculated with audio offload support considered. If this flag is set to true, the returned frame count is what it would be if the stream is activated for offload mode. However, if this flag is set to true but the audio endpoint does not support offload mode, then the flag has no effect. Use [ISpatialAudioClient2::IsOffloadCapable](nf-spatialaudioclient-ispatialaudioclient2-isoffloadcapable.md) to check if offload mode is supported.

### -param objectFormat [in]

A pointer to a <xref:NS:mmeapi.tWAVEFORMATEX> structure specifying the format of the audio stream for which support is queried.

### -param frameCountPerBuffer [out]

Receives a pointer to an **INT32** indicating the maximum supported frame count for the audio device and the specified input parameters.

## -returns

An HRESULT including the following values.

| Value | Description |
|-------|-------------|
| S_OK | Success |
| AUDCLNT_E_DEVICE_INVALIDATED | The audio device associated with the audio client has been invalidated. |


## -remarks

The value returned by this method can be used to allocate source buffer. This value will change if the endpoint cadence changes. The caller must specify same [AUDIO_STREAM_CATEGORY](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) and [WAVEFORMATEX](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) values that will be used when creating the stream. The *offloadEnabled* parameter must be set to TRUE if the stream will be created with the [SPATIAL_AUDIO_STREAM_OPTIONS_OFFLOAD](ne-spatialaudioclient-spatial_audio_stream_options) flag. 


## -see-also

