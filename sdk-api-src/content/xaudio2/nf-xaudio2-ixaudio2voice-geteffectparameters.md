---
UID: NF:xaudio2.IXAudio2Voice.GetEffectParameters
title: IXAudio2Voice::GetEffectParameters (xaudio2.h)
description: Returns the current effect-specific parameters of a given effect in the voice's effect chain.
helpviewer_keywords: ["GetEffectParameters","GetEffectParameters method [XAudio2 Audio Mixing APIs]","GetEffectParameters method [XAudio2 Audio Mixing APIs]","IXAudio2Voice interface","IXAudio2Voice interface [XAudio2 Audio Mixing APIs]","GetEffectParameters method","IXAudio2Voice.GetEffectParameters","IXAudio2Voice::GetEffectParameters","xaudio2.ixaudio2voice_interface_geteffectparameters","xaudio2/IXAudio2Voice::GetEffectParameters"]
old-location: xaudio2\ixaudio2voice_interface_geteffectparameters.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.GetEffectParameters(UINT32,void@,UINT32@)
ms.date: 12/05/2018
ms.keywords: GetEffectParameters, GetEffectParameters method [XAudio2 Audio Mixing APIs], GetEffectParameters method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, IXAudio2Voice interface [XAudio2 Audio Mixing APIs],GetEffectParameters method, IXAudio2Voice.GetEffectParameters, IXAudio2Voice::GetEffectParameters, xaudio2.ixaudio2voice_interface_geteffectparameters, xaudio2/IXAudio2Voice::GetEffectParameters
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAudio2Voice::GetEffectParameters
 - xaudio2/IXAudio2Voice::GetEffectParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAudio2.h
api_name:
 - IXAudio2Voice.GetEffectParameters
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

Returns S_OK if successful, an error code otherwise. See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of error codes.



Fails with E_NOTIMPL if the effect does not support a generic parameter control interface.

## -remarks

<b>GetEffectParameters</b> always returns the effect's actual current parameters. However, these may not match the parameters set by the most recent call to <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters">IXAudio2Voice::SetEffectParameters</a>: the actual parameters are only changed the next time the audio engine runs after the <b>IXAudio2Voice::SetEffectParameters</b> call (or after the corresponding <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges">IXAudio2::CommitChanges</a> call, if <b>IXAudio2Voice::SetEffectParameters</b> was called with a deferred operation ID).



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xapo/nf-xapo-ixapoparameters-getparameters">IXAPOParameters::GetParameters</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>



<a href="/windows/desktop/xaudio2/xapo-overview">XAPO Overview</a>