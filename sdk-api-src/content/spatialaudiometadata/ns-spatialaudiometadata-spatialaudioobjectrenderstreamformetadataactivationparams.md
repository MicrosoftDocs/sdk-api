---
UID: NS:spatialaudiometadata.SpatialAudioObjectRenderStreamForMetadataActivationParams
title: SpatialAudioObjectRenderStreamForMetadataActivationParams (spatialaudiometadata.h)
description: Represents activation parameters for a spatial audio render stream for metadata. Pass this structure to ISpatialAudioClient::ActivateSpatialAudioStream when activating a stream.helpviewer_keywords: ["PSpatialAudioObjectRenderStreamForMetadataActivationParams","PSpatialAudioObjectRenderStreamForMetadataActivationParams structure pointer [Core Audio]","SpatialAudioObjectRenderStreamForMetadataActivationParams","SpatialAudioObjectRenderStreamForMetadataActivationParams structure [Core Audio]","coreaudio.spatialaudioobjectrenderstreamformetadataactivationparams","spatialaudiometadata/PSpatialAudioObjectRenderStreamForMetadataActivationParams","spatialaudiometadata/SpatialAudioObjectRenderStreamForMetadataActivationParams"]
old-location: coreaudio\spatialaudioobjectrenderstreamformetadataactivationparams.htm
tech.root: CoreAudio
ms.assetid: 5B92F521-537F-4296-B9A7-7EC6985530B3
ms.date: 12/05/2018
ms.keywords: PSpatialAudioObjectRenderStreamForMetadataActivationParams, PSpatialAudioObjectRenderStreamForMetadataActivationParams structure pointer [Core Audio], SpatialAudioObjectRenderStreamForMetadataActivationParams, SpatialAudioObjectRenderStreamForMetadataActivationParams structure [Core Audio], coreaudio.spatialaudioobjectrenderstreamformetadataactivationparams, spatialaudiometadata/PSpatialAudioObjectRenderStreamForMetadataActivationParams, spatialaudiometadata/SpatialAudioObjectRenderStreamForMetadataActivationParams
f1_keywords:
- spatialaudiometadata/SpatialAudioObjectRenderStreamForMetadataActivationParams
dev_langs:
- c++
req.header: spatialaudiometadata.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- spatialaudiometadata.h
api_name:
- SpatialAudioObjectRenderStreamForMetadataActivationParams
targetos: Windows
req.typenames: SpatialAudioObjectRenderStreamForMetadataActivationParams
req.redist: 
ms.custom: 19H1
---

# SpatialAudioObjectRenderStreamForMetadataActivationParams structure


## -description


Represents activation parameters for a spatial audio render stream for metadata. Pass this structure to <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream">ISpatialAudioClient::ActivateSpatialAudioStream</a> when activating a stream.


## -struct-fields




### -field ObjectFormat

 Format descriptor for a single spatial audio object. All objects used by the stream must have the same format and the format must be of type <a href="/windows/win32/api/mmreg/ns-mmreg-waveformatex">WAVEFORMATEX</a> or <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-waveformatextensible">WAVEFORMATEXTENSIBLE</a>. 


### -field StaticObjectTypeMask

 A bitwise combination of <b>AudioObjectType</b> values indicating the set of static spatial audio channels that will be allowed by the activated stream. 


### -field MinDynamicObjectCount

 The minimum number of concurrent dynamic objects. If this number of dynamic audio objects can't be activated simultaneously, <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream">ISpatialAudioClient::ActivateSpatialAudioStream</a> will fail with this error <b>SPTLAUDCLNT_E_NO_MORE_OBJECTS</b>.


### -field MaxDynamicObjectCount

 The maximum number of concurrent dynamic objects that can be activated with <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream">ISpatialAudioObjectRenderStream</a>. 


### -field Category

 The category of the audio stream and its spatial audio objects. 


### -field EventHandle

 The event that will signal the client to provide more audio data. This handle will be duplicated internally before it is used.


### -field MetadataFormatId

 The identifier of  the metadata format for the currently active spatial rendering engine.


### -field MaxMetadataItemCount

The maximum number of metadata items per frame.


### -field MetadataActivationParams

Additional activation parameters.


### -field NotifyObject

 The object that provides notifications for spatial audio clients to respond to changes in the state of an  <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream">ISpatialAudioObjectRenderStream</a>. This object is used to notify clients that the number of dynamic spatial audio objects that can be activated concurrently is about to change.

