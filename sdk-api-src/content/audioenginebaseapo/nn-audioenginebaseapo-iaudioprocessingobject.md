---
UID: NN:audioenginebaseapo.IAudioProcessingObject
title: IAudioProcessingObject (audioenginebaseapo.h)
description: System Effects Audio Processing Objects (sAPOs) are typically used in or called from real-time process threads.
helpviewer_keywords: ["IAudioProcessingObject","IAudioProcessingObject interface [Audio Devices]","IAudioProcessingObject interface [Audio Devices]","described","audio.iaudioprocessingobject","audio_syseffects_r_7b8bb04d-2546-4fa3-ae7b-7e11df3b1e15.xml","audioenginebaseapo/IAudioProcessingObject"]
old-location: audio\iaudioprocessingobject.htm
tech.root: audio
ms.assetid: 71be0151-20dd-40e3-a478-d67e4d8d9c36
ms.date: 12/05/2018
ms.keywords: IAudioProcessingObject, IAudioProcessingObject interface [Audio Devices], IAudioProcessingObject interface [Audio Devices],described, audio.iaudioprocessingobject, audio_syseffects_r_7b8bb04d-2546-4fa3-ae7b-7e11df3b1e15.xml, audioenginebaseapo/IAudioProcessingObject
req.header: audioenginebaseapo.h
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
 - IAudioProcessingObject
 - audioenginebaseapo/IAudioProcessingObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioenginebaseapo.h
api_name:
 - IAudioProcessingObject
---

# IAudioProcessingObject interface


## -description

System Effects Audio Processing Objects (sAPOs) are typically used in or called from real-time process threads. However, it is sometimes necessary to use an sAPO in a non real-time mode. For example, when an sAPO is initialized, it is called from a non real-time thread. But when audio processing begins, the sAPO is called from a real-time thread. The <code>IAudioProcessingObject</code> interface exposes methods that enable a client to access the non real-time compliant parts of an sAPO.

The <code>IAudioProcessingObject</code> interface supports the following methods:
<dl>
<dd>

<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobject-getinputchannelcount">IAudioProcessingObject::GetInputChannelCount</a>


</dd>
<dd>

<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobject-getlatency">IAudioProcessingObject::GetLatency</a>


</dd>
<dd>

<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobject-getregistrationproperties">IAudioProcessingObject::GetRegistrationProperties</a>


</dd>
<dd>

<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobject-initialize">IAudioProcessingObject::Initialize</a>


</dd>
<dd>

<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobject-isinputformatsupported">IAudioProcessingObject::IsInputFormatSupported</a>


</dd>
<dd>

<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobject-isoutputformatsupported">IAudioProcessingObject::IsOutputFormatSupported</a>


</dd>
<dd>

<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobject-reset">IAudioProcessingObject::Reset</a>


</dd>
</dl>