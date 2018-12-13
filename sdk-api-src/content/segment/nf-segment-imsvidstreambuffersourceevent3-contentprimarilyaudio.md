---
UID: NF:segment.IMSVidStreamBufferSourceEvent3.ContentPrimarilyAudio
title: IMSVidStreamBufferSourceEvent3::ContentPrimarilyAudio
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\imsvidstreambuffersourceevent3_contentprimarilyaudio.htm
tech.root: mstv
ms.assetid: 5ee38fac-78f8-4130-8d16-db5380e11c5f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ContentPrimarilyAudio, ContentPrimarilyAudio method [Microsoft TV Technologies], ContentPrimarilyAudio method [Microsoft TV Technologies],IMSVidStreamBufferSourceEvent3 interface, IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies],ContentPrimarilyAudio method, IMSVidStreamBufferSourceEvent3.ContentPrimarilyAudio, IMSVidStreamBufferSourceEvent3::ContentPrimarilyAudio, IMSVidStreamBufferSourceEvent3ContentPrimarilyAudio, mstv.imsvidstreambuffersourceevent3_contentprimarilyaudio, segment/IMSVidStreamBufferSourceEvent3::ContentPrimarilyAudio
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMSVidStreamBufferSourceEvent3.ContentPrimarilyAudio
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidStreamBufferSourceEvent3::ContentPrimarilyAudio


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>ContentPrimarilyAudio</b> method is called when the Stream Buffer Engine is processing primarily audio data.


## -parameters






## -returns



Return S_OK or an error code.




## -remarks



This event is sent when the <a href="https://msdn.microsoft.com/4043e199-d329-45f3-80a7-cd84fad88979">MSVidStreamBufferSource</a> object receives an STREAMBUFFER_EC_PRIMARY_AUDIO event from the Stream Buffer Engine. For more information, see <a href="https://msdn.microsoft.com/84364aa4-7306-40ee-9f4d-0683c47965b5">Stream Buffer Engine Event Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd694672(v=VS.85).aspx">IMSVidStreamBufferSourceEvent3 Interface</a>
 

 

