---
UID: NS:spatialaudiohrtf.SpatialAudioHrtfActivationParams
title: SpatialAudioHrtfActivationParams
author: windows-sdk-content
description: Specifies the activation parameters for an ISpatialAudioRenderStreamForHrtf.
old-location: coreaudio\spatialaudiohrtfactivationparams.htm
tech.root: CoreAudio
ms.assetid: 6A549BFB-993A-4A20-AFAB-B38D03EAE35C
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: PSpatialAudioHrtfActivationParams, PSpatialAudioHrtfActivationParams structure pointer [Core Audio], SpatialAudioHrtfActivationParams, SpatialAudioHrtfActivationParams structure [Core Audio], coreaudio.spatialaudiohrtfactivationparams, spatialaudiohrtf/PSpatialAudioHrtfActivationParams, spatialaudiohrtf/SpatialAudioHrtfActivationParams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: spatialaudiohrtf.h
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
 - spatialaudiohrtf.h
api_name:
 - SpatialAudioHrtfActivationParams
product: Windows
targetos: Windows
req.typenames: SpatialAudioHrtfActivationParams
req.redist: 
---

# SpatialAudioHrtfActivationParams structure


## -description


Specifies the activation parameters for an <a href="https://msdn.microsoft.com/9DFEF82A-1571-47AB-BE0E-059BCCC8289A">ISpatialAudioRenderStreamForHrtf</a>.


## -struct-fields




### -field ObjectFormat

Format descriptor for spatial audio objects associated with the stream. All objects must have the same format and must be of type <a href="https://msdn.microsoft.com/4f3bf6fb-b15f-43b3-82f1-e7a8a3007057">WAVEFORMATEX</a> or <a href="https://msdn.microsoft.com/b16cdcab-fa4f-4c9a-b1f3-af459bd33245">WAVEFORMATEXTENSIBLE</a>.


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

