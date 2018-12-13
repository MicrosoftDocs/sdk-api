---
UID: NE:segment.MSVidSinkStreams
title: MSVidSinkStreams
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\msvidsinkstreams.htm
tech.root: mstv
ms.assetid: 11738d9f-25b1-4903-94a4-145202a81380
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Audio, MSVidSinkStreams, MSVidSinkStreams enumeration [Microsoft TV Technologies], MSVidSinkStreamsEnumeration, Other, Video, mstv.msvidsinkstreams, segment/Audio, segment/MSVidSinkStreams, segment/Other, segment/Video
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: segment.h
req.include-header: Dshow.h
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
 - segment.h
api_name:
 - MSVidSinkStreams
product: Windows
targetos: Windows
req.typenames: MSVidSinkStreams
req.redist: 
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
 

 

