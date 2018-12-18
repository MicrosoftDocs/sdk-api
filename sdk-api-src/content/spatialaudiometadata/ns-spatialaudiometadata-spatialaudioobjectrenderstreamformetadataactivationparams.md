---
UID: NS:spatialaudiometadata.SpatialAudioObjectRenderStreamForMetadataActivationParams
title: SpatialAudioObjectRenderStreamForMetadataActivationParams
author: windows-sdk-content
description: Represents activation parameters for a spatial audio render stream for metadata. Pass this structure to ISpatialAudioClient::ActivateSpatialAudioStream when activating a stream.
old-location: coreaudio\spatialaudioobjectrenderstreamformetadataactivationparams.htm
tech.root: CoreAudio
ms.assetid: 5B92F521-537F-4296-B9A7-7EC6985530B3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PSpatialAudioObjectRenderStreamForMetadataActivationParams, PSpatialAudioObjectRenderStreamForMetadataActivationParams structure pointer [Core Audio], SpatialAudioObjectRenderStreamForMetadataActivationParams, SpatialAudioObjectRenderStreamForMetadataActivationParams structure [Core Audio], coreaudio.spatialaudioobjectrenderstreamformetadataactivationparams, spatialaudiometadata/PSpatialAudioObjectRenderStreamForMetadataActivationParams, spatialaudiometadata/SpatialAudioObjectRenderStreamForMetadataActivationParams
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: SpatialAudioObjectRenderStreamForMetadataActivationParams
req.redist: 
---

# SpatialAudioObjectRenderStreamForMetadataActivationParams structure


## -description


Represents activation parameters for a spatial audio render stream for metadata. Pass this structure to <a href="https://msdn.microsoft.com/CBBB5A62-D342-4FB7-890C-9FE37949CC07">ISpatialAudioClient::ActivateSpatialAudioStream</a> when activating a stream.


## -struct-fields




### -field ObjectFormat

 Format descriptor for a single spatial audio object. All objects used by the stream must have the same format and the format must be of type <a href="https://msdn.microsoft.com/f2f050d6-afe2-4647-932b-1287f4538702">WAVEFORMATEX</a> or <a href="https://msdn.microsoft.com/54bcb18e-df4b-471c-b121-4db75ce5c49b">WAVEFORMATEXTENSIBLE</a>. 


### -field StaticObjectTypeMask

 A bitwise combination of <b>AudioObjectType</b> values indicating the set of static spatial audio channels that will be allowed by the activated stream. 


### -field MinDynamicObjectCount

 The minimum number of concurrent dynamic objects. If this number of dynamic audio objects can't be activated simultaneously, <a href="https://msdn.microsoft.com/CBBB5A62-D342-4FB7-890C-9FE37949CC07">ISpatialAudioClient::ActivateSpatialAudioStream</a> will fail with this error <b>SPTLAUDCLNT_E_NO_MORE_OBJECTS</b>.


### -field MaxDynamicObjectCount

 The maximum number of concurrent dynamic objects that can be activated with <a href="https://msdn.microsoft.com/B4D10CC6-62BF-4D20-910F-E39DF812010D">ISpatialAudioObjectRenderStream</a>. 


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

 The object that provides notifications for spatial audio clients to respond to changes in the state of an  <a href="https://msdn.microsoft.com/B4D10CC6-62BF-4D20-910F-E39DF812010D">ISpatialAudioObjectRenderStream</a>. This object is used to notify clients that the number of dynamic spatial audio objects that can be activated concurrently is about to change.

