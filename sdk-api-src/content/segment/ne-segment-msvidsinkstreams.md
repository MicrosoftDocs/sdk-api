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

# MSVidSinkStreams enumeration


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>MSVidSinkStreams</b> enumeration defines the stream types for a generic sink.


## -enum-fields




### -field MSVidSink_Video


### -field MSVidSink_Audio


### -field MSVidSink_Other




#### - Audio

Indicates an audio stream.


#### - Other

Indicates a stream that is neither video nor audio.


#### - Video

Indicates a video steam.


## -see-also




<a href="https://msdn.microsoft.com/e77f2ee8-081b-4415-87b5-ab27ee0218d2">IMSVidGenericSink::get_SinkStreams</a>



<a href="https://msdn.microsoft.com/a9bb76ad-6b10-4a48-9d94-64e6d28a3b9f">IMSVidGenericSink::put_SinkStreams</a>



<a href="https://msdn.microsoft.com/3c21f2c6-8eff-4fe5-a383-057f3394d9ee">Video Control Enumerations</a>
 

 

