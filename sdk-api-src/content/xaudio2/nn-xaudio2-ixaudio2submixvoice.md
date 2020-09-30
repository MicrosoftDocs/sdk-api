---
UID: NN:xaudio2.IXAudio2SubmixVoice
title: IXAudio2SubmixVoice (xaudio2.h)
description: A submix voice is used primarily for performance improvements and effects processing.
helpviewer_keywords: ["IXAudio2SubmixVoice","IXAudio2SubmixVoice interface [XAudio2 Audio Mixing APIs]","IXAudio2SubmixVoice interface [XAudio2 Audio Mixing APIs]","described","xaudio2.ixaudio2submixvoice","xaudio2/IXAudio2SubmixVoice"]
old-location: xaudio2\ixaudio2submixvoice.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixaudio2submixvoice.IXAudio2SubmixVoice
ms.date: 12/05/2018
ms.keywords: IXAudio2SubmixVoice, IXAudio2SubmixVoice interface [XAudio2 Audio Mixing APIs], IXAudio2SubmixVoice interface [XAudio2 Audio Mixing APIs],described, xaudio2.ixaudio2submixvoice, xaudio2/IXAudio2SubmixVoice
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
 - IXAudio2SubmixVoice
 - xaudio2/IXAudio2SubmixVoice
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
 - IXAudio2SubmixVoice
---

# IXAudio2SubmixVoice interface


## -description

A submix voice is used primarily for performance improvements and effects processing.

## -remarks

Data buffers cannot be submitted directly to submix voices and will not be audible unless submitted to a mastering voice. A submix voice can be used to ensure that a particular set of voice data is converted to the same format and/or to have a particular effect chain processed on the collective result. 


IXAudio2SubmixVoice inherits directly from <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>, but does not implement methods specific to submix voices. The interface type exists solely because some of the base class methods are implemented differently for submix voices. Having a separate type for these voices helps client code to distinguish the different voice types and to benefit from C++ type safety.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--use-submix-voices">How to: Use Submix Voices</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>



<a href="/windows/desktop/xaudio2/xapo-overview">XAPO Overview</a>



<a href="/windows/desktop/xaudio2/interfaces">XAudio2 Interfaces</a>