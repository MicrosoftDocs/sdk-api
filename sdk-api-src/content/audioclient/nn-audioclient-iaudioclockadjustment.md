---
UID: NN:audioclient.IAudioClockAdjustment
title: IAudioClockAdjustment (audioclient.h)
description: The IAudioClockAdjustment interface is used to adjust the sample rate of a stream.
helpviewer_keywords: ["IAudioClockAdjustment","IAudioClockAdjustment interface [Core Audio]","IAudioClockAdjustment interface [Core Audio]","described","audioclient/IAudioClockAdjustment","coreaudio.iaudioclockadjustment"]
old-location: coreaudio\iaudioclockadjustment.htm
tech.root: CoreAudio
ms.assetid: 61d90fd9-6c73-4987-b424-1523f15ab023
ms.date: 12/05/2018
ms.keywords: IAudioClockAdjustment, IAudioClockAdjustment interface [Core Audio], IAudioClockAdjustment interface [Core Audio],described, audioclient/IAudioClockAdjustment, coreaudio.iaudioclockadjustment
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
 - IAudioClockAdjustment
 - audioclient/IAudioClockAdjustment
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
 - IAudioClockAdjustment
---

# IAudioClockAdjustment interface


## -description

The <b>IAudioClockAdjustment</b> interface is used to adjust the sample rate of a stream. 
		

The client obtains a reference to the <b>IAudioClockAdjustment</b> interface of a stream object by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> method with parameter <i>riid</i> set to REFIID IID_IAudioClockAdjustment. Adjusting the sample rate is not supported for exclusive mode streams. 

The <b>IAudioClockAdjustment</b> interface must be obtained from an audio client that is initialized with both the AUDCLNT_STREAMFLAGS_RATEADJUST flag  and the share mode set to AUDCLNT_SHAREMODE_SHARED.
			  If <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">Initialize</a> is called in an exclusive mode with the AUDCLNT_STREAMFLAGS_RATEADJUST flag, <b>Initialize</b> fails with the  AUDCLNT_E_UNSUPPORTED_FORMAT error code.

When releasing an <b>IAudioClockAdjustment</b> interface instance, the client must call the interface's <b>Release</b> method from the same thread as the call to <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> that created the object.

## -inheritance

The <b>IAudioClockAdjustment</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioClockAdjustment</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/audclnt-streamflags-xxx-constants">AUDCLNT_STREAMFLAGS_XXX Constants</a>



<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>
