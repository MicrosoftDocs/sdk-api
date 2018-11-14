---
UID: NS:xaudio2.XAUDIO2_VOICE_SENDS
title: XAUDIO2_VOICE_SENDS
author: windows-sdk-content
description: Defines a set of voices to receive data from a single output voice.
old-location: xaudio2\xaudio2_voice_sends.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2_VOICE_SENDS
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: XAUDIO2_VOICE_SENDS, XAUDIO2_VOICE_SENDS structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2_voice_sends, xaudio2/XAUDIO2_VOICE_SENDS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - HeaderDef
api_location:
 - xaudio2.h
api_name:
 - XAUDIO2_VOICE_SENDS
product: Windows
targetos: Windows
req.typenames: XAUDIO2_VOICE_SENDS
req.redist: 
---

# XAUDIO2_VOICE_SENDS structure


## -description


Defines a set of voices to receive data from a single output voice.


## -struct-fields




### -field SendCount

Number of voices to receive the output of the voice. An <b>OutputCount</b> value of 0 indicates the voice should not send output to any voices.


### -field pSends

Array of <a href="https://msdn.microsoft.com/en-us/library/Ee419244(v=VS.85).aspx">XAUDIO2_SEND_DESCRIPTOR</a> structures describing destination voices and the filters that should be used when sending to the voices. This array should contain <b>SendCount</b> elements. If <b>SendCount</b> is 0 <b>pSends</b> should be NULL. Note that <b>pSends</b> cannot contain the same voice more than once.


## -remarks



If <b>pSends</b> is not NULL all of its elements must be non-NULL. To send output to the default mastering voice call <a href="https://msdn.microsoft.com/en-us/library/Ee418599(v=VS.85).aspx">IXAudio2Voice::SetOutputVoices</a> with the pSendList argument set to NULL.



Setting <b>SendCount</b> to 0 is useful for certain effects such as volume meters or file writers that don't generate any audio output to pass on to another voice.



If needed, a voice will perform a single sample rate conversion, from the voice's input sample rate to the input sample rate of the voice's output voices. Because only one sample rate conversion will be performed, all the voice's output voices must have the same input sample rate. If the input sample rates of the voice and its output voices are the same, no sample rate conversion is performed.


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/40004128-4abb-4bcd-fe76-91276be8abec">How to: Change Voice Volume</a>



<a href="https://msdn.microsoft.com/76c1c138-4846-9c4f-7875-446867436ee9">How to: Use Submix Voices</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee418607(v=VS.85).aspx">IXAudio2::CreateSourceVoice</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee418608(v=VS.85).aspx">IXAudio2::CreateSubmixVoice</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee418599(v=VS.85).aspx">IXAudio2Voice::SetOutputVoices</a>



<a href="https://msdn.microsoft.com/3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c">XAudio Structures</a>



<a href="https://msdn.microsoft.com/be34ce62-6552-45e2-a247-830ab55ea9ec">XAudio2 Sample Rate Conversions</a>
 

 

