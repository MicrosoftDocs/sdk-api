---
UID: NS:spatialaudioclient.SpatialAudioObjectRenderStreamActivationParams2
tech.root: CoreAudio
title: SpatialAudioObjectRenderStreamActivationParams2
ms.date: 01/31/2022
targetos: Windows
description: Represents activation parameters for a spatial audio render stream, extending SpatialAudioObjectRenderStreamActivationParams with the ability to specify stream options.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: spatialaudioclient.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.typenames: SpatialAudioObjectRenderStreamActivationParams2
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - spatialaudioclient.h
api_name:
 - SpatialAudioObjectRenderStreamActivationParams2
f1_keywords:
 - SpatialAudioObjectRenderStreamActivationParams2
 - spatialaudioclient/SpatialAudioObjectRenderStreamActivationParams2
dev_langs:
 - c++
---

## -description

Represents activation parameters for a spatial audio render stream, extending <xref:NS:spatialaudioclient.SpatialAudioObjectRenderStreamActivationParams> with the ability to specify stream options. Pass this structure to <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream">ISpatialAudioClient::ActivateSpatialAudioStream</a> when activating a stream.

## -struct-fields

### -field ObjectFormat

 Format descriptor for a single spatial audio object. All objects used by the stream must have the same format and the format must be of type <a href="/windows/win32/api/mmreg/ns-mmreg-waveformatex">WAVEFORMATEX</a> or <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-waveformatextensible">WAVEFORMATEXTENSIBLE</a>.

### -field StaticObjectTypeMask

 A bitwise combination of <b>AudioObjectType</b> values indicating the set of static spatial audio channels that will be allowed by the activated stream.

### -field MinDynamicObjectCount

The minimum number of concurrent dynamic objects. If this number of dynamic audio objects can't be activated simultaneously, <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream">ISpatialAudioClient::ActivateSpatialAudioStream</a> will fail with this error <b>SPTLAUDCLNT_E_NO_MORE_OBJECTS</b>.

### -field MaxDynamicObjectCount

The maximum number of concurrent dynamic objects that can be activated with <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream">ISpatialAudioObjectRenderStream</a>.

### -field Category

The category of the audio stream and its spatial audio objects.

### -field EventHandle

 The event that will signal the client to provide more audio data. This handle will be duplicated internally before it is used.

### -field NotifyObject

 The object that provides notifications for spatial audio clients to respond to changes in the state of an  <a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream">ISpatialAudioObjectRenderStream</a>. This object is used to notify clients that the number of dynamic spatial audio objects that can be activated concurrently is about to change.

### -field Options

A member of the [SPATIAL_AUDIO_STREAM_OPTIONS](ne-spatialaudioclient-spatial_audio_stream_options) emumeration, specifying options for the activated audio stream.

## -remarks

## -see-also

