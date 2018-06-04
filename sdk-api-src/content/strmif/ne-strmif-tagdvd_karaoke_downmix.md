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

# tagDVD_KARAOKE_DOWNMIX enumeration


## -description



Defines flags used by the <a href="https://msdn.microsoft.com/9101fd83-1349-4cdd-b5e9-6daeb7d1e3d8">IDvdControl2::SelectKaraokeAudioPresentationMode</a> method to control which speakers, if any, each auxiliary channel is downmixed to.




## -enum-fields




### -field DVD_Mix_0to0


            Reserved.
          


### -field DVD_Mix_1to0


            Reserved.
          


### -field DVD_Mix_2to0

Downmix channel 2 to the left speaker.


### -field DVD_Mix_3to0

Downmix channel 3 to the left speaker.


### -field DVD_Mix_4to0

Downmix channel 4 to the left speaker.


### -field DVD_Mix_Lto0


            Reserved.
          


### -field DVD_Mix_Rto0


            Reserved.
          


### -field DVD_Mix_0to1


            Reserved.
          


### -field DVD_Mix_1to1


            Reserved.
          


### -field DVD_Mix_2to1

Downmix channel 2 to the right speaker.


### -field DVD_Mix_3to1

Downmix channel 3 to the right speaker.


### -field DVD_Mix_4to1

Downmix channel 4 to the right speaker.


### -field DVD_Mix_Lto1


            Reserved.
          


### -field DVD_Mix_Rto1


            Reserved.
          


## -remarks



Audio channels are zero-based, so channels 2 through 4 are the three auxiliary karaoke channels. Use bitwise <b>OR</b> operations to set the appropriate bit to send a channel to the left speaker (0), right speaker (1), both speakers, or to no speakers by turning both bits off. These bits are all off by default whenever the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator Filter</a> filter enters karaoke mode.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/9101fd83-1349-4cdd-b5e9-6daeb7d1e3d8">IDvdControl2::SelectKaraokeAudioPresentationMode</a>
 

 

