---
UID: NF:xaudio2.IXAudio2SourceVoice.GetFrequencyRatio
title: IXAudio2SourceVoice::GetFrequencyRatio
author: windows-sdk-content
description: Returns the frequency adjustment ratio of the voice.
old-location: xaudio2\ixaudio2sourcevoice_interface_getfrequencyratio.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2sourcevoice.IXAudio2SourceVoice.GetFrequencyRatio(float@)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetFrequencyRatio, GetFrequencyRatio method [XAudio2 Audio Mixing APIs], GetFrequencyRatio method [XAudio2 Audio Mixing APIs],IXAudio2SourceVoice interface, IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs],GetFrequencyRatio method, IXAudio2SourceVoice.GetFrequencyRatio, IXAudio2SourceVoice::GetFrequencyRatio, xaudio2.ixaudio2sourcevoice_interface_getfrequencyratio, xaudio2/IXAudio2SourceVoice::GetFrequencyRatio
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
 - IXAudio2SourceVoice.GetFrequencyRatio
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
- IXAudio2SourceVoice.GetFrequencyRatio
: 
---

# IXAudio2SourceVoice::GetFrequencyRatio


## -description


Returns the frequency adjustment ratio of the voice.


## -parameters




### -param pRatio [out]

Returns the current frequency adjustment ratio if successful.


## -returns



This method does not return a value.




## -remarks



<b>GetFrequencyRatio</b> always returns the voice's actual current frequency ratio. However, this may not match the ratio set by the most recent <a href="https://msdn.microsoft.com/en-us/library/Ee418469(v=VS.85).aspx">IXAudio2SourceVoice::SetFrequencyRatio</a> call: the actual ratio is only changed the next time the audio engine runs after the <b>IXAudio2SourceVoice::SetFrequencyRatio</b> call (or after the corresponding <a href="https://msdn.microsoft.com/en-us/library/Ee418603(v=VS.85).aspx">IXAudio2::CommitChanges</a> call, if <b>IXAudio2SourceVoice::SetFrequencyRatio</b> was called with a deferred operation ID).



For information on frequency ratios, see <a href="https://msdn.microsoft.com/en-us/library/Ee418469(v=VS.85).aspx">IXAudio2SourceVoice::SetFrequencyRatio</a>.


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee415914(v=VS.85).aspx">IXAudio2SourceVoice</a>
 

 

