---
UID: NN:audioclient.IAudioClock2
title: IAudioClock2 (audioclient.h)
description: The IAudioClock2 interface is used to get the current device position.
helpviewer_keywords: ["IAudioClock2","IAudioClock2 interface [Core Audio]","IAudioClock2 interface [Core Audio]","described","audioclient/IAudioClock2","coreaudio.iaudioclock2"]
old-location: coreaudio\iaudioclock2.htm
tech.root: CoreAudio
ms.assetid: 4820c93a-a5d8-4ab9-aefc-9377fc76e745
ms.date: 12/05/2018
ms.keywords: IAudioClock2, IAudioClock2 interface [Core Audio], IAudioClock2 interface [Core Audio],described, audioclient/IAudioClock2, coreaudio.iaudioclock2
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IAudioClock2
 - audioclient/IAudioClock2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioclient.h
api_name:
 - IAudioClock2
---

# IAudioClock2 interface


## -description

The <b>IAudioClock2</b> interface is used to get the current device position.
		

To get a reference to the <b>IAudioClock2</b> interface, the application must call <b>IAudioClock::QueryInterface</b> to request the interface pointer from the stream object's  <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclock">IAudioClock</a> interface.
	

The client obtains a reference to the <b>IAudioClock</b> interface of a stream object by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> method with parameter <i>riid</i> set to REFIID IID_IAudioClock.
	

When releasing an <b>IAudioClock2</b> interface instance, the client must call the interface's <b>Release</b> method from the same thread as the call to <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> that created the object.

## -inheritance

The <b>IAudioClock2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioClock2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclock">IAudioClock</a>
