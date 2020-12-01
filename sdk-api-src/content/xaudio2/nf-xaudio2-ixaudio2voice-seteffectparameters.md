---
UID: NF:xaudio2.IXAudio2Voice.SetEffectParameters
title: IXAudio2Voice::SetEffectParameters (xaudio2.h)
description: Sets parameters for a given effect in the voice's effect chain.
helpviewer_keywords: ["IXAudio2Voice interface [XAudio2 Audio Mixing APIs]","SetEffectParameters method","IXAudio2Voice.SetEffectParameters","IXAudio2Voice::SetEffectParameters","SetEffectParameters","SetEffectParameters method [XAudio2 Audio Mixing APIs]","SetEffectParameters method [XAudio2 Audio Mixing APIs]","IXAudio2Voice interface","xaudio2.ixaudio2voice_interface_seteffectparameters","xaudio2/IXAudio2Voice::SetEffectParameters"]
old-location: xaudio2\ixaudio2voice_interface_seteffectparameters.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.SetEffectParameters(UINT32,const void,UINT32,UINT32)
ms.date: 12/05/2018
ms.keywords: IXAudio2Voice interface [XAudio2 Audio Mixing APIs],SetEffectParameters method, IXAudio2Voice.SetEffectParameters, IXAudio2Voice::SetEffectParameters, SetEffectParameters, SetEffectParameters method [XAudio2 Audio Mixing APIs], SetEffectParameters method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, xaudio2.ixaudio2voice_interface_seteffectparameters, xaudio2/IXAudio2Voice::SetEffectParameters
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
 - IXAudio2Voice::SetEffectParameters
 - xaudio2/IXAudio2Voice::SetEffectParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2Voice.SetEffectParameters
---

# IXAudio2Voice::SetEffectParameters


## -description

Sets parameters for a given effect in the voice's effect chain.

## -parameters

### -param EffectIndex [in]

Zero-based index of an effect within the voice's effect chain.

### -param pParameters [in]

Returns the current values of the effect-specific parameters.

### -param ParametersByteSize [in]

Size of the <b>pParameters</b> array in bytes.

### -param X2DEFAULT

TBD

### -param OperationSet [in]

Identifies this call as part of a deferred batch. See the <a href="/windows/desktop/xaudio2/xaudio2-operation-sets">XAudio2 Operation Sets</a> overview for more information.

## -returns

Returns S_OK if successful; otherwise, an error code. See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of error codes.



Fails with E_NOTIMPL if the effect does not support a generic parameter control interface.

## -remarks

The specific effect being used determines the valid size and format of the <i>pParameters</i> buffer. The call will fail if <i>pParameters</i> is invalid or if <i>ParametersByteSize</i> is not exactly the size that the effect expects. The client must take care to direct the <b>SetEffectParameters</b> call to the right effect. If this call is directed to a different effect that happens to accept the same parameter block size, the parameters will be interpreted differently. This may lead to unexpected results.



The memory pointed to by <i>pParameters</i> must <i>not</i> be freed immediately, because XAudio2 will need to refer to it later when the parameters actually are applied to the effect. This happens during the next audio processing pass if the <i>OperationSet</i> argument is <b>XAUDIO2_COMMIT_NOW</b>. Otherwise, the parameters are applied to the effect later, during the first processing pass after the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges">IXAudio2::CommitChanges</a> function is called with the same <i>OperationSet</i> argument.



<b>SetEffectParameters</b> takes effect immediately when called from an XAudio2 callback with an <i>OperationSet</i> of <b>XAUDIO2_COMMIT_NOW</b>.


<div class="alert"><b>Note</b>  <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-geteffectparameters">IXAudio2Voice::GetEffectParameters</a> always returns the effect's actual current parameters. However, these may not match the parameters set by the most recent call to <b>IXAudio2Voice::SetEffectParameters</b>. The actual parameters are only changed the next time the audio engine runs after the <b>IXAudio2Voice::SetEffectParameters</b> call (or after the corresponding <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges">IXAudio2::CommitChanges</a> call, if <b>IXAudio2Voice::SetEffectParameters</b> was called with a deferred operation ID).</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--create-an-effect-chain">How to: Create an Effect Chain</a>



<a href="/windows/desktop/api/xapo/nf-xapo-ixapoparameters-setparameters">IXAPOParameters::SetParameters</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>



<a href="/windows/desktop/xaudio2/xapo-overview">XAPO Overview</a>