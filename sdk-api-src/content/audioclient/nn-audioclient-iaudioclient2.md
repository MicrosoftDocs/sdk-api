---
UID: NN:audioclient.IAudioClient2
title: IAudioClient2 (audioclient.h)
description: The IAudioClient2 interface is derived from the IAudioClient interface, with a set of additional methods that enable a Windows Audio Session API (WASAPI) audio client to do the following:\_opt in for offloading, query stream properties, and get information from the hardware that handles offloading.The audio client can be successful in creating an offloaded stream if the underlying endpoint supports the hardware audio engine, the endpoint has been enumerated and discovered by the audio system, and there are still offload pin instances available on the endpoint.
helpviewer_keywords: ["IAudioClient2","IAudioClient2 interface [Core Audio]","IAudioClient2 interface [Core Audio]","described","audioclient/IAudioClient2","coreaudio.iaudioclient2"]
old-location: coreaudio\iaudioclient2.htm
tech.root: CoreAudio
ms.assetid: 9CE79CEB-115E-4802-A687-B2CB23E6A0E0
ms.date: 12/05/2018
ms.keywords: IAudioClient2, IAudioClient2 interface [Core Audio], IAudioClient2 interface [Core Audio],described, audioclient/IAudioClient2, coreaudio.iaudioclient2
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IAudioClient2
 - audioclient/IAudioClient2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioclient.h
api_name:
 - IAudioClient2
---

# IAudioClient2 interface


## -description

The <b>IAudioClient2</b> interface is derived from the <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a> interface, with a set of additional methods that enable a Windows Audio Session API (WASAPI) audio client to do the following: opt in for offloading, query stream properties, and get information from the hardware that handles offloading.The audio client can be successful in creating an offloaded stream if the underlying endpoint supports the hardware audio engine, the endpoint has been enumerated and discovered by the audio system, and there are still offload pin instances available on the endpoint.</p>

## -inheritance

The <b>IAudioClient2</b> interface inherits from the <a href="/windows/win32/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a> interface. <b>IAudioClient2</b> also has these types of members:

## -see-also

<a href="/windows/win32/api/audioclient/ns-audioclient-audioclientproperties~r1">AudioClientProperties</a>



<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a>
