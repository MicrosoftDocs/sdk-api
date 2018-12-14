---
UID: NF:xaudio2.IXAudio2Voice.GetEffectState
title: IXAudio2Voice::GetEffectState
author: windows-sdk-content
description: Returns the running state of the effect at a specified position in the effect chain of the voice.
old-location: xaudio2\ixaudio2voice_interface_geteffectstate.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.GetEffectState(UINT32,BOOL@)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetEffectState, GetEffectState method [XAudio2 Audio Mixing APIs], GetEffectState method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, IXAudio2Voice interface [XAudio2 Audio Mixing APIs],GetEffectState method, IXAudio2Voice.GetEffectState, IXAudio2Voice::GetEffectState, xaudio2.ixaudio2voice_interface_geteffectstate, xaudio2/IXAudio2Voice::GetEffectState
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
 - XAudio2.h
api_name:
 - IXAudio2Voice.GetEffectState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXAudio2Voice::GetEffectState


## -description


Returns the running state of the effect at a specified position in the effect chain of the voice.


## -parameters




### -param EffectIndex [in]

Zero-based index of an effect in the effect chain of the voice.


### -param pEnabled [out]

Returns TRUE If the effect is enabled. If the effect is disabled, returns FALSE.


## -returns



This method does not return a value.




## -remarks



<b>GetEffectState</b> always returns the effect's actual current state. However, this may not be the state set by the most recent <a href="https://msdn.microsoft.com/en-us/library/Ee418584(v=VS.85).aspx">IXAudio2Voice::EnableEffect</a> or <a href="https://msdn.microsoft.com/en-us/library/Ee418583(v=VS.85).aspx">IXAudio2Voice::DisableEffect</a> call: the actual state is only changed the next time the audio engine runs after the <b>IXAudio2Voice::EnableEffect</b> or <b>IXAudio2Voice::DisableEffect</b> call (or after the corresponding <a href="https://msdn.microsoft.com/en-us/library/Ee418603(v=VS.85).aspx">IXAudio2::CommitChanges</a> call, if EnableEffect/DisableEffect was called with a deferred operation ID).

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee415917(v=VS.85).aspx">IXAudio2Voice</a>



<a href="https://msdn.microsoft.com/4fe88a0f-0234-462f-b575-e592f2c8401e">XAPO Overview</a>
 

 

