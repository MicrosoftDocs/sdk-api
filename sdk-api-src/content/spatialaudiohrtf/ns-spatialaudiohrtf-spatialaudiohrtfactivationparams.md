---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# SpatialAudioHrtfActivationParams structure


## -description


Specifies the activation parameters for an <a href="https://msdn.microsoft.com/9DFEF82A-1571-47AB-BE0E-059BCCC8289A">ISpatialAudioRenderStreamForHrtf</a>.


## -struct-fields




### -field ObjectFormat

Format descriptor for spatial audio objects associated with the stream. All objects must have the same format and must be of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff538802">WAVEFORMATEXTENSIBLE</a>.


### -field StaticObjectTypeMask

 A bitwise combination of <b>AudioObjectType</b> values indicating the set of static spatial audio channels that will be allowed by the activated stream. 


### -field MinDynamicObjectCount

 The minimum number of concurrent dynamic objects. If this number of dynamic audio objects can't be activated simultaneously, no dynamic audio objects will be activated. 


### -field MaxDynamicObjectCount

 The maximum number of concurrent dynamic objects that can be activated with <a href="https://msdn.microsoft.com/9DFEF82A-1571-47AB-BE0E-059BCCC8289A">ISpatialAudioRenderStreamForHrtf</a>. 


### -field Category

 The category of the audio stream and its spatial audio objects. 


### -field EventHandle

 The event that will signal the client to provide more audio data. This handle will be duplicated internally before it is used.


### -field NotifyObject

 The object that provides notifications for spatial audio clients to respond to changes in the state of an  <a href="https://msdn.microsoft.com/9DFEF82A-1571-47AB-BE0E-059BCCC8289A">ISpatialAudioRenderStreamForHrtf</a>. This object is used to notify clients that the number of dynamic spatial audio objects that can be activated concurrently is about to change.


### -field DistanceDecay

Optional default value for the decay model used for <a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a> objects associated with the stream. <b>nullptr</b> if unused.


### -field Directivity

Optional default value for the spatial audio directivity model used for <a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a> objects associated with the stream. <b>nullptr</b> if unused.


### -field Environment

Optional default value for the type of environment that is simulated when audio is processed for <a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a> objects associated with the stream. <b>nullptr</b> if unused.


### -field Orientation

Optional default value for the orientation of <a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a> objects associated with the stream. <b>nullptr</b> if unused.

