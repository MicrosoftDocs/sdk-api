---
UID: NF:segment.IMSVidPlaybackEvent.EndOfMedia
title: IMSVidPlaybackEvent::EndOfMedia (segment.h)
author: windows-sdk-content
description: This topic applies to Windows XP or later.
old-location: mstv\imsvidplaybackevent_endofmedia.htm
tech.root: mstv
ms.assetid: 00c73b5e-dc0f-4ffd-930f-e93ce3d1e179
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EndOfMedia, EndOfMedia method [Microsoft TV Technologies], EndOfMedia method [Microsoft TV Technologies],IMSVidPlaybackEvent interface, IMSVidPlaybackEvent interface [Microsoft TV Technologies],EndOfMedia method, IMSVidPlaybackEvent.EndOfMedia, IMSVidPlaybackEvent::EndOfMedia, IMSVidPlaybackEventEndOfMedia, mstv.imsvidplaybackevent_endofmedia, segment/IMSVidPlaybackEvent::EndOfMedia
ms.topic: method
f1_keywords: 
 - "segment/IMSVidPlaybackEvent.EndOfMedia"
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidPlaybackEvent.EndOfMedia
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidPlaybackEvent::EndOfMedia


## -description



This topic applies to Windows XP or later.
        



The <b>EndOfMedia</b> method is called when playback reaches the end of the source media.


## -parameters




### -param lpd [in]

Specifies a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidplayback">IMSVidPlayback</a> interface of the playback device.


## -returns



Return S_OK or an error code.




## -remarks



The dispatch identifier (dispid) of this method is <b>eventidEndOfMedia</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidplaybackevent">IMSVidPlaybackEvent Interface</a>
 

 

