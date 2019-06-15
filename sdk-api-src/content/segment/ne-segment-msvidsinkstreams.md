---
UID: NE:segment.MSVidSinkStreams
title: MSVidSinkStreams (segment.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\msvidsinkstreams.htm
tech.root: mstv
ms.assetid: 11738d9f-25b1-4903-94a4-145202a81380
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Audio, MSVidSinkStreams, MSVidSinkStreams enumeration [Microsoft TV Technologies], MSVidSinkStreamsEnumeration, Other, Video, mstv.msvidsinkstreams, segment/Audio, segment/MSVidSinkStreams, segment/Other, segment/Video
ms.topic: enum
f1_keywords: ["segment/MSVidSinkStreams"]
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
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidgenericsink-get_sinkstreams">IMSVidGenericSink::get_SinkStreams</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidgenericsink-put_sinkstreams">IMSVidGenericSink::put_SinkStreams</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-enumerations">Video Control Enumerations</a>
 

 

