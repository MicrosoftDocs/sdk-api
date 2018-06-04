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

# tagAM_DvdKaraokeData structure


## -description



Specifies how to mix the karaoke audio channels.




## -struct-fields




### -field dwDownmix

A bitwise OR of <a href="https://msdn.microsoft.com/7f0132ae-6a46-4b81-9c5b-a0399a429b1a">DVD_KARAOKE_DOWNMIX</a> flags telling the decoder which channels are downmixed to channels 0 or 1.


### -field dwSpeakerAssignment

A valid <a href="https://msdn.microsoft.com/cdfd05b9-7a4a-49cc-ab50-bbe83ed9e0f0">DVD_KARAOKE_ASSIGNMENT</a> value that indicates which speakers the output is going to.


## -remarks



This structure is used for the AM_PROPERTY_DVDKARAOKE_DATA property.




## -see-also




<a href="https://msdn.microsoft.com/78b2998b-d8b3-424d-85bc-872e64eb4a4f">DVD Karaoke Property Set</a>



<a href="https://msdn.microsoft.com/9101fd83-1349-4cdd-b5e9-6daeb7d1e3d8">SelectKaraokeAudioPresentationMode</a>
 

 

