---
UID: NF:xaudio2.IXAudio2Voice.GetVolume
title: IXAudio2Voice::GetVolume
author: windows-sdk-content
description: Gets the current overall volume level of the voice.
old-location: xaudio2\ixaudio2voice_interface_getvolume.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.GetVolume(float@)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetVolume, GetVolume method [XAudio2 Audio Mixing APIs], GetVolume method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, IXAudio2Voice interface [XAudio2 Audio Mixing APIs],GetVolume method, IXAudio2Voice.GetVolume, IXAudio2Voice::GetVolume, xaudio2.ixaudio2voice_interface_getvolume, xaudio2/IXAudio2Voice::GetVolume
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
 - IXAudio2Voice.GetVolume
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
- IXAudio2Voice.GetVolume
: 
---

# IXAudio2Voice::GetVolume


## -description


Gets the current overall volume level of the voice.


## -parameters




### -param pVolume [out]

Returns the current overall volume level of the voice. See Remarks for more information on volume levels.


## -returns



This method does not return a value.




## -remarks



Volume levels are expressed as floating-point amplitude multipliers between -224 to 224, with a maximum gain of 144.5 dB. A volume level of 1 means there is no attenuation or gain and 0 means silence. Negative levels can be used to invert the audio's phase. See <a href="https://msdn.microsoft.com/dedc2d01-af83-d7d2-5b64-743dcebc83f7">XAudio2 Volume and Pitch Control</a> for additional information on volume control.



<div class="alert"><b>Note</b>  <b>GetVolume</b> always returns the volume most recently set by <a href="https://msdn.microsoft.com/D744E313-4281-4184-97E9-3FAB0F652871">IXAudio2Voice::SetVolume</a>. However, it may not actually be in effect yet: it only takes effect the next time the audio engine runs after the <b>IXAudio2Voice::SetVolume</b> call (or after the corresponding <a href="https://msdn.microsoft.com/2E798B7B-AD3E-4DCD-BB88-BAD3EC64EFE1">IXAudio2::CommitChanges</a> call, if <b>IXAudio2Voice::SetVolume</b> was called with a deferred operation ID).</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/F704008E-AE43-4189-8B34-8E3915338627">IXAudio2Voice</a>
 

 

