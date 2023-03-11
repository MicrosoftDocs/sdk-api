---
UID: NE:spatialaudioclient.SPATIAL_AUDIO_STREAM_OPTIONS
tech.root: CoreAudio
title: SPATIAL_AUDIO_STREAM_OPTIONS
ms.date: 08/16/2022
targetos: Windows
description: Specifies audio stream options for calls to ActivateSpatialAudioStream.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: spatialaudioclient.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - spatialaudioclient.h
api_name:
 - SPATIAL_AUDIO_STREAM_OPTIONS
f1_keywords:
 - SPATIAL_AUDIO_STREAM_OPTIONS
 - spatialaudioclient/SPATIAL_AUDIO_STREAM_OPTIONS
dev_langs:
 - c++
---

## -description

Specifies audio stream options for calls to <xref:NF:spatialaudioclient.ISpatialAudioClient.ActivateSpatialAudioStream>.

## -enum-fields

### -field SPATIAL_AUDIO_STREAM_OPTIONS_NONE

No stream options.

### -field SPATIAL_AUDIO_STREAM_OPTIONS_OFFLOAD

The stream should support audio offloading. For more information, see <xref:NN:spatialaudioclient.ISpatialAudioClient2>.

## -remarks

This enumeration value is used by the version 2 structures for spatial audio activation parameters.

- <xref:NS:spatialaudioclient.SpatialAudioObjectRenderStreamActivationParams2>
- <xref:NS:spatialaudiohrtf.SpatialAudioHrtfActivationParams2>
- <xref:NS:spatialaudiometadata.SpatialAudioObjectRenderStreamForMetadataActivationParams2>
- 
## -see-also

