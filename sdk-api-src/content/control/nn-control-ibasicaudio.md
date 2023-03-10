---
UID: NN:control.IBasicAudio
title: IBasicAudio (control.h)
description: The IBasicAudio interface controls the volume and balance of the audio stream.This interface is implemented on the Audio Renderer (WaveOut) filter and the DirectSound Renderer filter, but is exposed to applications through the Filter Graph Manager.
helpviewer_keywords: ["IBasicAudio","IBasicAudio interface [DirectShow]","IBasicAudio interface [DirectShow]","described","IBasicAudioInterface","control/IBasicAudio","dshow.ibasicaudio"]
old-location: dshow\ibasicaudio.htm
tech.root: dshow
ms.assetid: 0335b263-8d32-4690-a606-ba2b3e382680
ms.date: 12/05/2018
ms.keywords: IBasicAudio, IBasicAudio interface [DirectShow], IBasicAudio interface [DirectShow],described, IBasicAudioInterface, control/IBasicAudio, dshow.ibasicaudio
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBasicAudio
 - control/IBasicAudio
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IBasicAudio
---

# IBasicAudio interface


## -description

The <code>IBasicAudio</code> interface controls the volume and balance of the audio stream.

This interface is implemented on the <a href="/windows/desktop/DirectShow/audio-renderer--waveout--filter">Audio Renderer (WaveOut)</a> filter and the <a href="/windows/desktop/DirectShow/directsound-renderer-filter">DirectSound Renderer</a> filter, but is exposed to applications through the Filter Graph Manager. Applications should always retrieve this interface from the Filter Graph Manager.

## -inheritance

The <b>IBasicAudio</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IBasicAudio</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
