---
UID: NN:xaudio2.IXAudio2MasteringVoice
title: IXAudio2MasteringVoice (xaudio2.h)
description: A mastering voice is used to represent the audio output device.
helpviewer_keywords: ["IXAudio2MasteringVoice","IXAudio2MasteringVoice interface [XAudio2 Audio Mixing APIs]","IXAudio2MasteringVoice interface [XAudio2 Audio Mixing APIs]","described","xaudio2.ixaudio2masteringvoice","xaudio2/IXAudio2MasteringVoice"]
old-location: xaudio2\ixaudio2masteringvoice.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixaudio2masteringvoice.IXAudio2MasteringVoice
ms.date: 12/05/2018
ms.keywords: IXAudio2MasteringVoice, IXAudio2MasteringVoice interface [XAudio2 Audio Mixing APIs], IXAudio2MasteringVoice interface [XAudio2 Audio Mixing APIs],described, xaudio2.ixaudio2masteringvoice, xaudio2/IXAudio2MasteringVoice
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
req.lib: Xaudio2.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAudio2MasteringVoice
 - xaudio2/IXAudio2MasteringVoice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.lib
 - xaudio2.dll
api_name:
 - IXAudio2MasteringVoice
---

# IXAudio2MasteringVoice interface


## -description

A mastering voice is used to represent the audio output device.

Data buffers cannot be submitted directly to mastering voices, but data submitted to other types of voices must be directed to a mastering voice to be heard. 


<b>IXAudio2MasteringVoice</b> inherits directly from <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>, but does not implement methods specific to mastering voices. The interface type exists solely because some of the base class methods are implemented differently for mastering voices. Having a separate type for these voices helps client code to distinguish the different voice types and to benefit from C++ type safety.

## -inheritance

The <b>IXAudio2MasteringVoice</b> interface inherits from <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>. <b>IXAudio2MasteringVoice</b> also has these types of members:

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>



<a href="/windows/desktop/xaudio2/interfaces">XAudio2 Interfaces</a>
