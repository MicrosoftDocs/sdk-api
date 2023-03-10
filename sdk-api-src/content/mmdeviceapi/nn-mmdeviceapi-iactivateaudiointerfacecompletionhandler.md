---
UID: NN:mmdeviceapi.IActivateAudioInterfaceCompletionHandler
title: IActivateAudioInterfaceCompletionHandler (mmdeviceapi.h)
description: Provides a callback to indicate that activation of a WASAPI interface is complete.
helpviewer_keywords: ["IActivateAudioInterfaceCompletionHandler","IActivateAudioInterfaceCompletionHandler interface [Core Audio]","IActivateAudioInterfaceCompletionHandler interface [Core Audio]","described","coreaudio.iactivateaudiointerfacecompletionhandler","mmdeviceapi/IActivateAudioInterfaceCompletionHandler"]
old-location: coreaudio\iactivateaudiointerfacecompletionhandler.htm
tech.root: CoreAudio
ms.assetid: 04ff7cbb-fd33-40d9-9c11-4f716c6423b0
ms.date: 12/05/2018
ms.keywords: IActivateAudioInterfaceCompletionHandler, IActivateAudioInterfaceCompletionHandler interface [Core Audio], IActivateAudioInterfaceCompletionHandler interface [Core Audio],described, coreaudio.iactivateaudiointerfacecompletionhandler, mmdeviceapi/IActivateAudioInterfaceCompletionHandler
req.header: mmdeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mmdeviceapi.idl
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
 - IActivateAudioInterfaceCompletionHandler
 - mmdeviceapi/IActivateAudioInterfaceCompletionHandler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmdeviceapi.h
api_name:
 - IActivateAudioInterfaceCompletionHandler
---

# IActivateAudioInterfaceCompletionHandler interface


## -description

Provides a callback to indicate that activation of a <a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a> interface is complete.

## -inheritance

The <b>IActivateAudioInterfaceCompletionHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IActivateAudioInterfaceCompletionHandler</b> also has these types of members:

## -remarks

<b>When to implement:</b>  
An application implements this interface if it calls the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync">ActivateAudioInterfaceAsync</a> function.


The implementation must be agile (aggregating a free-threaded marshaler).

## -see-also

<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync">ActivateAudioInterfaceAsync</a>



<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation">IActivateAudioInterfaceAsyncOperation</a>
