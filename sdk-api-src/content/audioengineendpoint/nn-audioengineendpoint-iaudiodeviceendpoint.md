---
UID: NN:audioengineendpoint.IAudioDeviceEndpoint
title: IAudioDeviceEndpoint (audioengineendpoint.h)
description: Initializes a device endpoint object and gets the capabilities of the device that it represents.
helpviewer_keywords: ["IAudioDeviceEndpoint","IAudioDeviceEndpoint interface [Remote Desktop Services]","IAudioDeviceEndpoint interface [Remote Desktop Services]","described","audioengineendpoint/IAudioDeviceEndpoint","termserv.iaudiodeviceendpoint"]
old-location: termserv\iaudiodeviceendpoint.htm
tech.root: TermServ
ms.assetid: 3112bc7e-e138-4b42-8f82-61fdf19f7e94
ms.date: 12/05/2018
ms.keywords: IAudioDeviceEndpoint, IAudioDeviceEndpoint interface [Remote Desktop Services], IAudioDeviceEndpoint interface [Remote Desktop Services],described, audioengineendpoint/IAudioDeviceEndpoint, termserv.iaudiodeviceendpoint
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
 - IAudioDeviceEndpoint
 - audioengineendpoint/IAudioDeviceEndpoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioDeviceEndpoint
---

# IAudioDeviceEndpoint interface


## -description

Initializes a device endpoint object and gets the capabilities of the device that it represents.

A <i>device endpoint</i> abstracts an audio device. The device can be a rendering device such as a speaker or a capture  device such as a microphone. A device endpoint must implement the <b>IAudioDeviceEndpoint</b> interface.
      

To a get a reference to the <b>IAudioDeviceEndpoint</b> interface of the device, the audio engine calls <b>QueryInterface</b> on the audio endpoint (<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt">IAudioInputEndpointRT</a> or <a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt">IAudioOutputEndpointRT</a>) for the device.

## -inheritance

The <b>IAudioDeviceEndpoint</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioDeviceEndpoint</b> also has these types of members:

## -remarks

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.
