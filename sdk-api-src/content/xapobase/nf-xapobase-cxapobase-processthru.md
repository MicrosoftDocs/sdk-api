---
UID: NF:xapobase.CXAPOBase.ProcessThru
title: CXAPOBase::ProcessThru
author: windows-sdk-content
description: Called by an IXAPO::Process implementation when an XAPO is disabled for thru processing.
old-location: xaudio2\cxapobase_processthru.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.cxapobase.CXAPOBase.ProcessThru(void,FLOAT32,UINT32,WORD,WORD,BOOL)
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: CXAPOBase interface [XAudio2 Audio Mixing APIs],ProcessThru method, CXAPOBase.ProcessThru, CXAPOBase::ProcessThru, ProcessThru, ProcessThru method [XAudio2 Audio Mixing APIs], ProcessThru method [XAudio2 Audio Mixing APIs],CXAPOBase interface, xapobase/CXAPOBase::ProcessThru, xaudio2.cxapobase_processthru
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xapobase.h
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
tech.root: 
req.typenames: XAPO_REGISTRATION_PROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPOBase.lib
 - XAPOBase.dll
api_name:
 - CXAPOBase.ProcessThru
product: Windows
targetos: Windows
req.lib: XAPOBase.lib
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# CXAPOBase::ProcessThru


## -description


Called by an <a href="https://msdn.microsoft.com/2510590D-578A-4A39-847A-34DFE620A7CC">IXAPO::Process</a> implementation when an XAPO is disabled for thru processing.


## -parameters




### -param pInputBuffer

Pointer to a buffer containing the input audio data.


### -param pOutputBuffer

Pointer to a buffer that will contain the processed audio data.


### -param FrameCount

Number of frames of audio data to process, where a frame is a block of samples, one per channel of audio data.


### -param InputChannelCount

Number of channels in the input data buffer.



### -param OutputChannelCount

Number of channels in the output data buffer.


### -param MixWithOutput






#### - MixWithDestination

TRUE to mix with the destination buffer, FALSE to overwrite the destination buffer.



## -returns



This method does not return a value.




## -remarks



<b>ProcessThru</b> copies/mixes data from source to destination, making as few changes as possible to the audio data. However, <b>ProcessThru</b> is capable of channel upmix/downmix and uses the same matrix coefficient table used by windows Vista to do so.



This function may be called if:

<ol>
<li>The XAPO is locked and disabled.

</li>
<li>The number of source frames equals the number of destination frames.

</li>
<li>The output format is FLOAT32.

</li>
<li>input format is INT8, INT16, INT20 (contained in 24 or 32 bits), INT24 (contained in 24 or 32 bits), INT32, or FLOAT32.</li>
</ol>

For in-place processing (where the input buffer equals the output buffer) this function does nothing.



When writing a <b>ProcessThru</b> method it is important to note XAudio2 audio data is interleaved, data from each channel is adjacent for a particular sample number. For example if there was a 4 channel wave playing into an XAudio2 source voice, the audio data would be a sample of channel 0, a sample of channel 1, a sample of channel 2, a sample of channel 3, and then the next sample of channels 0, 1, 2, 3, etc.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/C55C4597-F379-462E-94FE-D7CF2004D8F4">CXAPOBase</a>



<a href="https://msdn.microsoft.com/21DA61D2-8EDE-496B-8513-D67121697FBA">IXAPO</a>
 

 

