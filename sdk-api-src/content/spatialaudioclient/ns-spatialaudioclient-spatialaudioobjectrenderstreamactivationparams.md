---
UID: NS:spatialaudioclient.SpatialAudioObjectRenderStreamActivationParams
title: SpatialAudioObjectRenderStreamActivationParams (spatialaudioclient.h)
description: Represents activation parameters for a spatial audio render stream. Pass this structure to ISpatialAudioClient::ActivateSpatialAudioStream when activating a stream.
helpviewer_keywords: ["PSpatialAudioObjectRenderStreamActivationParams","PSpatialAudioObjectRenderStreamActivationParams structure pointer [Core Audio]","SpatialAudioObjectRenderStreamActivationParams","SpatialAudioObjectRenderStreamActivationParams","SpatialAudioObjectRenderStreamActivationParams structure [Core Audio]","coreaudio.spatialaudioobjectrenderstreamactivationparams_","spatialaudioclient/PSpatialAudioObjectRenderStreamActivationParams","spatialaudioclient/SpatialAudioObjectRenderStreamActivationParams"]
old-location: coreaudio\spatialaudioobjectrenderstreamactivationparams_.htm
tech.root: CoreAudio
ms.assetid: DD27FDE1-3B4B-4C11-A980-15AF60A3A75B
ms.date: 12/05/2018
ms.keywords: PSpatialAudioObjectRenderStreamActivationParams, PSpatialAudioObjectRenderStreamActivationParams structure pointer [Core Audio], SpatialAudioObjectRenderStreamActivationParams, SpatialAudioObjectRenderStreamActivationParams , SpatialAudioObjectRenderStreamActivationParams structure [Core Audio], coreaudio.spatialaudioobjectrenderstreamactivationparams_, spatialaudioclient/PSpatialAudioObjectRenderStreamActivationParams, spatialaudioclient/SpatialAudioObjectRenderStreamActivationParams
req.header: spatialaudioclient.h
req.include-header: 
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
req.typenames: SpatialAudioObjectRenderStreamActivationParams
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SpatialAudioObjectRenderStreamActivationParams
 - spatialaudioclient/SpatialAudioObjectRenderStreamActivationParams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - spatialaudioclient.h
api_name:
 - SpatialAudioObjectRenderStreamActivationParams
---

# SpatialAudioObjectRenderStreamActivationParams structure


## -description

Represents activation parameters for a spatial audio render stream. Pass this structure to <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream">ISpatialAudioClient::ActivateSpatialAudioStream</a> when activating a stream.

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