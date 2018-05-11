---
UID: NS:spatialaudioclient.SpatialAudioObjectRenderStreamActivationParams
title: SpatialAudioObjectRenderStreamActivationParams
author: windows-driver-content
description: Represents activation parameters for a spatial audio render stream. Pass this structure to ISpatialAudioClient::ActivateSpatialAudioStream when activating a stream.
old-location: coreaudio\spatialaudioobjectrenderstreamactivationparams_.htm
old-project: CoreAudio
ms.assetid: DD27FDE1-3B4B-4C11-A980-15AF60A3A75B
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: PSpatialAudioObjectRenderStreamActivationParams, PSpatialAudioObjectRenderStreamActivationParams structure pointer [Core Audio], SpatialAudioObjectRenderStreamActivationParams, SpatialAudioObjectRenderStreamActivationParams , SpatialAudioObjectRenderStreamActivationParams structure [Core Audio], coreaudio.spatialaudioobjectrenderstreamactivationparams_, spatialaudioclient/PSpatialAudioObjectRenderStreamActivationParams, spatialaudioclient/SpatialAudioObjectRenderStreamActivationParams
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: SpatialAudioObjectRenderStreamActivationParams
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	spatialaudioclient.h
api_name:
-	SpatialAudioObjectRenderStreamActivationParams
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# SpatialAudioObjectRenderStreamActivationParams structure


## -description


Represents activation parameters for a spatial audio render stream. Pass this structure to <a href="https://msdn.microsoft.com/CBBB5A62-D342-4FB7-890C-9FE37949CC07">ISpatialAudioClient::ActivateSpatialAudioStream</a> when activating a stream. 


## -struct-fields




### -field ObjectFormat

 Format descriptor for a single spatial audio object. All objects used by the stream must have the same format and the format must be of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff538802">WAVEFORMATEXTENSIBLE</a>. 


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


### -field NotifyObject

 The object that provides notifications for spatial audio clients to respond to changes in the state of an  <a href="https://msdn.microsoft.com/B4D10CC6-62BF-4D20-910F-E39DF812010D">ISpatialAudioObjectRenderStream</a>. This object is used to notify clients that the number of dynamic spatial audio objects that can be activated concurrently is about to change.

