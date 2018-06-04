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

# tagDVD_AUDIO_APPMODE enumeration


## -description



Indicates the current audio mode as retrieved in a call to <a href="https://msdn.microsoft.com/80291efa-f3eb-47f0-94e0-dcde583ff35c">IDvdInfo2::GetAudioAttributes</a>.




## -enum-fields




### -field DVD_AudioMode_None


            No special audio mode. The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator Filter</a> will send the audio to the decoder with no special processing.
          


### -field DVD_AudioMode_Karaoke


            The current audio mode is karaoke content.
          


### -field DVD_AudioMode_Surround


            The current audio mode is surround sound.
          


### -field DVD_AudioMode_Other


            Unrecognized audio mode.
          


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/80291efa-f3eb-47f0-94e0-dcde583ff35c">IDvdInfo2::GetAudioAttributes</a>
 

 

