---
UID: NS:xaudio2.XAUDIO2_EFFECT_CHAIN
title: XAUDIO2_EFFECT_CHAIN (xaudio2.h)
description: Defines an effect chain.
helpviewer_keywords: ["XAUDIO2_EFFECT_CHAIN","XAUDIO2_EFFECT_CHAIN structure [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2_effect_chain","xaudio2/XAUDIO2_EFFECT_CHAIN"]
old-location: xaudio2\xaudio2_effect_chain.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2_EFFECT_CHAIN
ms.date: 12/05/2018
ms.keywords: XAUDIO2_EFFECT_CHAIN, XAUDIO2_EFFECT_CHAIN structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2_effect_chain, xaudio2/XAUDIO2_EFFECT_CHAIN
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
req.typenames: XAUDIO2_EFFECT_CHAIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAUDIO2_EFFECT_CHAIN
 - xaudio2/XAUDIO2_EFFECT_CHAIN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xaudio2.h
api_name:
 - XAUDIO2_EFFECT_CHAIN
---

# XAUDIO2_EFFECT_CHAIN structure


## -description

Defines an effect chain.

## -struct-fields

### -field EffectCount

Number of effects in the effect chain for the voice.

### -field pEffectDescriptors

Array of <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor">XAUDIO2_EFFECT_DESCRIPTOR</a> structures containing pointers to XAPO instances.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--create-an-effect-chain">How to: Create an Effect Chain</a>



<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice">IXAudio2::CreateMasteringVoice</a>



<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice">IXAudio2::CreateSourceVoice</a>



<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice">IXAudio2::CreateSubmixVoice</a>



<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain">IXAudio2Voice::SetEffectChain</a>



<a href="/windows/desktop/xaudio2/xapo-overview">XAPO Overview</a>



<a href="/windows/desktop/xaudio2/structures">XAudio2 Structures</a>