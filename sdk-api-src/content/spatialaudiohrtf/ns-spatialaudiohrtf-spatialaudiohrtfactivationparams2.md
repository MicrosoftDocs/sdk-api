---
UID: NS:spatialaudiohrtf.SpatialAudioHrtfActivationParams2
tech.root: CoreAudio
title: SpatialAudioHrtfActivationParams2
ms.date: 01/31/2022
targetos: Windows
description: Represents activation parameters for a spatial audio render stream, extending SpatialAudioHrtfActivationParams with the ability to specify stream options. 
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: spatialaudiohrtf.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.typenames: SpatialAudioHrtfActivationParams2
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - spatialaudiohrtf.h
api_name:
 - SpatialAudioHrtfActivationParams2
f1_keywords:
 - SpatialAudioHrtfActivationParams2
 - spatialaudiohrtf/SpatialAudioHrtfActivationParams2
dev_langs:
 - c++
---

## -description

Represents activation parameters for a spatial audio render stream, extending <xref:NS:spatialaudiohrtf.SpatialAudioHrtfActivationParams> with the ability to specify stream options. 

## -struct-fields

### -field ObjectFormat

Format descriptor for spatial audio objects associated with the stream. All objects must have the same format and must be of type <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> or <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)">WAVEFORMATEXTENSIBLE</a>.

### -field StaticObjectTypeMask

 A bitwise combination of <b>AudioObjectType</b> values indicating the set of static spatial audio channels that will be allowed by the activated stream.

### -field MinDynamicObjectCount

 The minimum number of concurrent dynamic objects. If this number of dynamic audio objects can't be activated simultaneously, no dynamic audio objects will be activated.

### -field MaxDynamicObjectCount

 The maximum number of concurrent dynamic objects that can be activated with <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf">ISpatialAudioRenderStreamForHrtf</a>.

### -field Category

 The category of the audio stream and its spatial audio objects.

### -field EventHandle

The event that will signal the client to provide more audio data. This handle will be duplicated internally before it is used.

### -field NotifyObject

 The object that provides notifications for spatial audio clients to respond to changes in the state of an  <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf">ISpatialAudioRenderStreamForHrtf</a>. This object is used to notify clients that the number of dynamic spatial audio objects that can be activated concurrently is about to change.

### -field DistanceDecay

Optional default value for the decay model used for <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> objects associated with the stream. <b>nullptr</b> if unused.

### -field Directivity

Optional default value for the spatial audio directivity model used for <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> objects associated with the stream. <b>nullptr</b> if unused.

### -field Environment

Optional default value for the type of environment that is simulated when audio is processed for <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> objects associated with the stream. <b>nullptr</b> if unused.

### -field Orientation

Optional default value for the orientation of <a href="/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf">ISpatialAudioObjectForHrtf</a> objects associated with the stream. <b>nullptr</b> if unused.

### -field Options

A member of the <xref:NE:spatialaudioclient.SPATIAL_AUDIO_STREAM_OPTIONS> emumeration, specifying options for the activated audio stream.

## -remarks

The following example demostrates activating a spatial audio render stream for HRTF with stream options.

```cpp
void CreateSpatialAudioObjectRenderStreamForHrtf(
    _In_ ISpatialAudioClient2* spatialAudioClient,
    _In_ WAVEFORMATEX const* objectFormat,
    AudioObjectType staticObjectTypeMask,
    UINT32 minDynamicObjectCount,
    UINT32 maxDynamicObjectCount,
    AUDIO_STREAM_CATEGORY streamCategory,
    _In_ HANDLE eventHandle,
    _In_opt_ ISpatialAudioObjectRenderStreamNotify* notifyObject,
    _In_opt_ SpatialAudioHrtfDistanceDecay* distanceDecay,
    _In_opt_ SpatialAudioHrtfDirectivityUnion* directivity,
    _In_opt_ SpatialAudioHrtfEnvironmentType* environment,
    _In_opt_ SpatialAudioHrtfOrientation* orientation,
    bool enableOffload,
    _COM_Outptr_ ISpatialAudioObjectRenderStreamForHrtf** stream)
{
    SpatialAudioHrtfActivationParams2 streamActivationParams =
    {
        objectFormat,
        staticObjectTypeMask,
        minDynamicObjectCount,
        maxDynamicObjectCount,
        streamCategory,
        eventHandle,
        notifyObject,
        distanceDecay,
        directivity,
        environment,
        orientation,
        enableOffload ? SPATIAL_AUDIO_STREAM_OPTIONS_OFFLOAD : SPATIAL_AUDIO_STREAM_OPTIONS_NONE
    };

    PROPVARIANT activateParamsPropVariant = {};
    activateParamsPropVariant.vt = VT_BLOB;
    activateParamsPropVariant.blob.cbSize = sizeof(streamActivationParams);
    activateParamsPropVariant.blob.pBlobData = reinterpret_cast<BYTE*>(&streamActivationParams);

    *stream = nullptr;
    THROW_IF_FAILED(spatialAudioClient->ActivateSpatialAudioStream(&activateParamsPropVariant, IID_PPV_ARGS(stream)));
}

```

## -see-also



