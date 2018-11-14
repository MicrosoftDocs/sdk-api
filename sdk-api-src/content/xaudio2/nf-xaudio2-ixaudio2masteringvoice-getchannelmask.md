---
UID: NF:xaudio2.IXAudio2MasteringVoice.GetChannelMask
title: IXAudio2MasteringVoice::GetChannelMask
author: windows-sdk-content
description: Returns the channel mask for this voice.
old-location: xaudio2\ixaudio2masteringvoice_interface_getchannelmask.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2masteringvoice.IXAudio2MasteringVoice.GetChannelMask(DWORD@)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetChannelMask, GetChannelMask method [XAudio2 Audio Mixing APIs], GetChannelMask method [XAudio2 Audio Mixing APIs],IXAudio2MasteringVoice interface, IXAudio2MasteringVoice interface [XAudio2 Audio Mixing APIs],GetChannelMask method, IXAudio2MasteringVoice.GetChannelMask, IXAudio2MasteringVoice::GetChannelMask, xaudio2.ixaudio2masteringvoice_interface_getchannelmask, xaudio2/IXAudio2MasteringVoice::GetChannelMask
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
 - IXAudio2MasteringVoice.GetChannelMask
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
- IXAudio2MasteringVoice.GetChannelMask
: 
---

# IXAudio2MasteringVoice::GetChannelMask


## -description


Returns the channel mask for this voice.


## -parameters




### -param pChannelmask

TBD




#### - pChannelMask [out]

Returns the channel mask for this voice. This corresponds to the <b>dwChannelMask</b> member of the  <a href="https://msdn.microsoft.com/54bcb18e-df4b-471c-b121-4db75ce5c49b">WAVEFORMATEXTENSIBLE</a> structure. 



## -returns



This method does not return a value.




## -remarks



The <i>pChannelMask</i> argument is a bit-mask of the various channels in the speaker geometry reported by the audio system. This information is needed for the <a href="https://msdn.microsoft.com/20f3d374-60bd-4a8c-8bd2-32e3be729779">X3DAudioInitialize</a> <i>SpeakerChannelMask</i> parameter.



The X3DAUDIO.H header declares a number of <b>SPEAKER_</b> positional defines to decode these channels masks.



Examples include:



<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>SPEAKER_STEREO // SPEAKER_FRONT_LEFT (0x1) | SPEAKER_FRONT_RIGHT (0x2) 

SPEAKER_5POINT1 // SPEAKER_FRONT_LEFT (0x1) | SPEAKER_FRONT_RIGHT (0x2)
                                    // | SPEAKER_FRONT_CENTER (0x4)
                                    // | SPEAKER_LOW_FREQUENCY (0x8)
                                    // | SPEAKER_BACK_LEFT (0x10) | SPEAKER_BACK_RIGHT (0x20)</pre>
</td>
</tr>
</table></span></div>
<div class="alert"><b>Note</b>  For the DirectX SDK versions of XAUDIO, the channel mask for the output device was obtained via the <b>IXAudio2::GetDeviceDetails</b> method, which doesn't exist in Windows 8 and later.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8)




## -see-also




<a href="https://msdn.microsoft.com/96D8A15E-5090-4D67-982D-ACE99CEC4379">IXAudio2MasteringVoice</a>
 

 

