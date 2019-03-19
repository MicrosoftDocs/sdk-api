---
UID: NF:xaudio2.IXAudio2Voice.GetEffectParameters
title: IXAudio2Voice::GetEffectParameters (xaudio2.h)
author: windows-sdk-content
description: Returns the current effect-specific parameters of a given effect in the voice's effect chain.
old-location: xaudio2\ixaudio2voice_interface_geteffectparameters.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.GetEffectParameters(UINT32,void@,UINT32@)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetEffectParameters, GetEffectParameters method [XAudio2 Audio Mixing APIs], GetEffectParameters method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, IXAudio2Voice interface [XAudio2 Audio Mixing APIs],GetEffectParameters method, IXAudio2Voice.GetEffectParameters, IXAudio2Voice::GetEffectParameters, xaudio2.ixaudio2voice_interface_geteffectparameters, xaudio2/IXAudio2Voice::GetEffectParameters
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
 - IXAudio2Voice.GetEffectParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXAudio2Voice::GetEffectParameters


## -description


Returns the current effect-specific parameters of a given effect in the voice's effect chain.


## -parameters




### -param EffectIndex [in]

Zero-based index of an effect within the voice's effect chain.


### -param pParameters [out]

Returns the current values of the effect-specific parameters.


### -param ParametersByteSize [out]

Size, in bytes, of the pParameters array.


## -returns



Returns S_OK if successful, an error code otherwise. See <a href="https://msdn.microsoft.com/42a1c21c-4b14-114a-d79e-15a61eb2139b">XAudio2 Error Codes</a> for descriptions of error codes.



Fails with E_NOTIMPL if the effect does not support a generic parameter control interface.




## -remarks



<b>GetEffectParameters</b> always returns the effect's actual current parameters. However, these may not match the parameters set by the most recent call to <a href="https://msdn.microsoft.com/en-us/library/Ee418595(v=VS.85).aspx">IXAudio2Voice::SetEffectParameters</a>: the actual parameters are only changed the next time the audio engine runs after the <b>IXAudio2Voice::SetEffectParameters</b> call (or after the corresponding <a href="https://msdn.microsoft.com/en-us/library/Ee418603(v=VS.85).aspx">IXAudio2::CommitChanges</a> call, if <b>IXAudio2Voice::SetEffectParameters</b> was called with a deferred operation ID).



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee418443(v=VS.85).aspx">IXAPOParameters::GetParameters</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415917(v=VS.85).aspx">IXAudio2Voice</a>



<a href="https://msdn.microsoft.com/4fe88a0f-0234-462f-b575-e592f2c8401e">XAPO Overview</a>
 

 

