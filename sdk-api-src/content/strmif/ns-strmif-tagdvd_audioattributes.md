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

# tagDVD_AudioAttributes structure


## -description



The <code>DVD_AudioAttributes</code> structure is used in <a href="https://msdn.microsoft.com/80291efa-f3eb-47f0-94e0-dcde583ff35c">IDvdInfo2::GetAudioAttributes</a> to receive the various audio attributes of the disc.




## -struct-fields




### -field AppMode

Indicates the current audio mode. If the mode returned is DVD_AudioMode_Karaoke, call <a href="https://msdn.microsoft.com/c69ea1e0-8d8a-4cd3-86a4-a2d481160a2e">IDvdInfo2::GetKaraokeAttributes</a> to get more info.


### -field AppModeData

 


### -field AudioFormat

Describes the format (encoding mode) of the audio stream.


### -field Language

An <b>LCID</b> value indicating the language of the audio stream. Is zero if no language is present.


### -field LanguageExtension

A <a href="https://msdn.microsoft.com/01d82199-18e1-4d84-add1-f4f6790155c8">DVD_AUDIO_LANG_EXT</a> enumeration that will be filled in if any information is available on the disc.


### -field fHasMultichannelInfo

Indicates whether multichannel attributes are present. If <b>TRUE</b>, it means there is additional mixing information available, such as for SurroundSound. Call <a href="https://msdn.microsoft.com/4e901e14-9e98-4ca5-ae37-7a4564b187ab">IDvdInfo2::GetTitleAttributes</a> to retrieve the multichannel information.


### -field dwFrequency

The frequency in hertz (48k, 96k) of the audio stream.


### -field bQuantization

The resolution of the audio stream (16, 20, 24 bits, or other) Zero indicates the resolution is unknown.


### -field bNumberOfChannels

The number of channels. For example, 5.1 Dolby AC-3 has six channels.


### -field dwReserved


            Reserved.
          


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

