---
UID: NN:audioengineendpoint.IAudioEndpointLastBufferControl
title: IAudioEndpointLastBufferControl (audioengineendpoint.h)
description: Provides functionality to allow an offload stream client to notify the endpoint that the last buffer has been sent only partially filled.
helpviewer_keywords: ["IAudioEndpointLastBufferControl","IAudioEndpointLastBufferControl interface [Core Audio]","IAudioEndpointLastBufferControl interface [Core Audio]","described","audioengineendpoint/IAudioEndpointLastBufferControl","coreaudio.iaudioendpointlastbuffercontrol"]
old-location: coreaudio\iaudioendpointlastbuffercontrol.htm
tech.root: CoreAudio
ms.assetid: 79f4b370-fd04-41a9-ad74-54f7edd084c2
ms.date: 12/05/2018
ms.keywords: IAudioEndpointLastBufferControl, IAudioEndpointLastBufferControl interface [Core Audio], IAudioEndpointLastBufferControl interface [Core Audio],described, audioengineendpoint/IAudioEndpointLastBufferControl, coreaudio.iaudioendpointlastbuffercontrol
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AudioEngineEndpoint.idl
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
 - IAudioEndpointLastBufferControl
 - audioengineendpoint/IAudioEndpointLastBufferControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioengineendpoint.h
api_name:
 - IAudioEndpointLastBufferControl
---

# IAudioEndpointLastBufferControl interface


## -description

Provides functionality to allow an offload stream client to notify  the endpoint that the last buffer has been sent only partially filled.

## -inheritance

The <b>IAudioEndpointLastBufferControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioEndpointLastBufferControl</b> also has these types of members:

## -remarks

This is an optional interface on an endpoint.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>
