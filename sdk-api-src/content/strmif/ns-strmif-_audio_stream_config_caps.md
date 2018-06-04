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

# _AUDIO_STREAM_CONFIG_CAPS structure


## -description



The <b>AUDIO_STREAM_CONFIG_CAPS</b> structure describes a range of audio formats. Audio compression and capture filters use this structure to describe the formats they can produce.




## -struct-fields




### -field guid

Will be set to MEDIATYPE_Audio to indicate an audio sample.


### -field MinimumChannels

Minimum number of channels.


### -field MaximumChannels

Maximum number of channels.


### -field ChannelsGranularity

Granularity of the channels. For example, the filter might specify channels 2 through 4, in steps of 2.


### -field MinimumBitsPerSample

Minimum bits per sample.


### -field MaximumBitsPerSample

Maximum bits per sample.


### -field BitsPerSampleGranularity

Granularity of the bits per sample. For example, the filter might specify 8 bits per sample through 32 bits per sample, in steps of 8.


### -field MinimumSampleFrequency

Minimum sample frequency.


### -field MaximumSampleFrequency

Maximum sample frequency.


### -field SampleFrequencyGranularity

Granularity of the frequency. For example, the filter might specify 11025 Hz to 44100 Hz, in steps of 11025 Hz.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/9dd84847-2cae-42f2-a858-7106cd2ac075">IAMStreamConfig::GetStreamCaps</a>
 

 

