---
UID: NF:segment.IMSVidStreamBufferV2SourceEvent.ContentPrimarilyAudio
title: IMSVidStreamBufferV2SourceEvent::ContentPrimarilyAudio
author: windows-sdk-content
description: Fired when an SBE2 source filter receives a STREAMBUFFER_EC_PRIMARY_AUDIO event, which is fired through the IMSVidStreamBufferSourceEvent3 interface, and indicates that SBE is processing primarily audio data.
old-location: mstv\imsvidstreambufferv2sourceevent_contentprimarilyaudio.htm
tech.root: mstv
ms.assetid: 9056bed3-b4da-4eca-a573-0d9bda3d2127
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ContentPrimarilyAudio, ContentPrimarilyAudio method [Microsoft TV Technologies], ContentPrimarilyAudio method [Microsoft TV Technologies],IMSVidStreamBufferV2SourceEvent interface, IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],ContentPrimarilyAudio method, IMSVidStreamBufferV2SourceEvent.ContentPrimarilyAudio, IMSVidStreamBufferV2SourceEvent::ContentPrimarilyAudio, mstv.imsvidstreambufferv2sourceevent_contentprimarilyaudio, segment/IMSVidStreamBufferV2SourceEvent::ContentPrimarilyAudio
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IMSVidStreamBufferV2SourceEvent.ContentPrimarilyAudio
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidStreamBufferV2SourceEvent::ContentPrimarilyAudio


## -description


Fired when an SBE2 source filter receives a <b>STREAMBUFFER_EC_PRIMARY_AUDIO</b> event, which is fired through the <a href="https://msdn.microsoft.com/en-us/library/Dd694672(v=VS.85).aspx">IMSVidStreamBufferSourceEvent3</a> interface, and indicates that SBE is processing primarily audio data.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A STREAMBUFFER_EC_PRIMARY_AUDIO event is sent if video samples are captured at a low frame rate. This event generally occurs with audio services on a DVB stream, but it might also indicate a problem with capturing or encoding the video. 

This event applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd694694(v=VS.85).aspx">IMSVidStreamBufferV2SourceEvent</a>



<a href="https://msdn.microsoft.com/84364aa4-7306-40ee-9f4d-0683c47965b5">Stream Buffer Engine Event Codes</a>
 

 

