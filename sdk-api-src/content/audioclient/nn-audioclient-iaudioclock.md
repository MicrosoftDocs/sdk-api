---
UID: NN:audioclient.IAudioClock
title: IAudioClock (audioclient.h)
description: The IAudioClock interface enables a client to monitor a stream's data rate and the current position in the stream.
helpviewer_keywords: ["IAudioClock","IAudioClock interface [Core Audio]","IAudioClock interface [Core Audio]","described","audioclient/IAudioClock","coreaudio.iaudioclock"]
old-location: coreaudio\iaudioclock.htm
tech.root: CoreAudio
ms.assetid: dbec9468-b555-42a0-a988-dec3a66c9f96
ms.date: 12/05/2018
ms.keywords: IAudioClock, IAudioClock interface [Core Audio], IAudioClock interface [Core Audio],described, audioclient/IAudioClock, coreaudio.iaudioclock
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IAudioClock
 - audioclient/IAudioClock
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
 - IAudioClock
---

# IAudioClock interface


## -description

The <b>IAudioClock</b> interface enables a client to monitor a stream's data rate and the current position in the stream. The client obtains a reference to the <b>IAudioClock</b> interface of a stream object by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> method with parameter <i>riid</i> set to REFIID IID_IAudioClock.

When releasing an <b>IAudioClock</b> interface instance, the client must call the interface's Release method from the same thread as the call to <b>IAudioClient::GetService</b> that created the object.

## -inheritance

The <b>IAudioClock</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioClock</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a>



<a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a>
