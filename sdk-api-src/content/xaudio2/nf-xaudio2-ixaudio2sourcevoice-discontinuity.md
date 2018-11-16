---
UID: NF:xaudio2.IXAudio2SourceVoice.Discontinuity
title: IXAudio2SourceVoice::Discontinuity
author: windows-sdk-content
description: Notifies an XAudio2 voice that no more buffers are coming after the last one that is currently in its queue.
old-location: xaudio2\ixaudio2sourcevoice_interface_discontinuity_.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2sourcevoice.IXAudio2SourceVoice.Discontinuity
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Discontinuity, Discontinuity method [XAudio2 Audio Mixing APIs], Discontinuity method [XAudio2 Audio Mixing APIs],IXAudio2SourceVoice interface, IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs],Discontinuity method, IXAudio2SourceVoice.Discontinuity, IXAudio2SourceVoice::Discontinuity, xaudio2.ixaudio2sourcevoice_interface_discontinuity_, xaudio2/IXAudio2SourceVoice::Discontinuity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xaudio2.h
req.include-header: 
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
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2SourceVoice.Discontinuity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xaudio2.h
: 
- IXAudio2SourceVoice.Discontinuity
: 
---

# IXAudio2SourceVoice::Discontinuity


## -description


Notifies an XAudio2 voice that no more buffers are coming after the last one that is currently in its queue.


## -parameters






## -returns



Returns S_OK if successful, an error code otherwise.




## -remarks



<b>Discontinuity</b> suppresses the warnings that normally occur in the debug build of XAudio2 when a voice runs out of audio buffers to play. It is preferable to mark the final buffer of a stream by tagging it with the XAUDIO2_END_OF_STREAM flag, but in some cases the client may not know that a buffer is the end of a stream until after the buffer has been submitted.



Because calling <b>Discontinuity</b> is equivalent to applying the XAUDIO2_END_OF_STREAM flag retroactively to the last buffer submitted, an <a href="https://msdn.microsoft.com/852FBAA1-F390-441F-96DE-5086FB644B44">OnStreamEnd</a> callback will be made when this buffer completes.


<div class="alert"><b>Note</b>  XAudio2 may consume its entire buffer queue and emit a warning before the <b>Discontinuity</b> call takes effect, so <b>Discontinuity</b> is not guaranteed to suppress the warnings.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/116DD0E0-8F0B-4934-A48D-FDBE0D0DF049">IXAudio2SourceVoice</a>
 

 

