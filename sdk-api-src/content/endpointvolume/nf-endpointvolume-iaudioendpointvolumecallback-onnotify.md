---
UID: NF:endpointvolume.IAudioEndpointVolumeCallback.OnNotify
title: IAudioEndpointVolumeCallback::OnNotify (endpointvolume.h)
description: The OnNotify method notifies the client that the volume level or muting state of the audio endpoint device has changed.
helpviewer_keywords: ["IAudioEndpointVolumeCallback interface [Core Audio]","OnNotify method","IAudioEndpointVolumeCallback.OnNotify","IAudioEndpointVolumeCallback::OnNotify","IAudioEndpointVolumeCallbackOnNotify","OnNotify","OnNotify method [Core Audio]","OnNotify method [Core Audio]","IAudioEndpointVolumeCallback interface","coreaudio.iaudioendpointvolumecallback_onnotify","endpointvolume/IAudioEndpointVolumeCallback::OnNotify"]
old-location: coreaudio\iaudioendpointvolumecallback_onnotify.htm
tech.root: CoreAudio
ms.assetid: a8ffad44-c621-4335-a312-16e7d6af2c18
ms.date: 12/05/2018
ms.keywords: IAudioEndpointVolumeCallback interface [Core Audio],OnNotify method, IAudioEndpointVolumeCallback.OnNotify, IAudioEndpointVolumeCallback::OnNotify, IAudioEndpointVolumeCallbackOnNotify, OnNotify, OnNotify method [Core Audio], OnNotify method [Core Audio],IAudioEndpointVolumeCallback interface, coreaudio.iaudioendpointvolumecallback_onnotify, endpointvolume/IAudioEndpointVolumeCallback::OnNotify
req.header: endpointvolume.h
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
 - IAudioEndpointVolumeCallback::OnNotify
 - endpointvolume/IAudioEndpointVolumeCallback::OnNotify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Endpointvolume.h
api_name:
 - IAudioEndpointVolumeCallback.OnNotify
---

# IAudioEndpointVolumeCallback::OnNotify


## -description

The <b>OnNotify</b> method notifies the client that the volume level or muting state of the audio endpoint device has changed.

## -parameters

### -param pNotify [in]

Pointer to the volume-notification data. This parameter points to a structure of type <a href="/windows/desktop/api/endpointvolume/ns-endpointvolume-audio_volume_notification_data">AUDIO_VOLUME_NOTIFICATION_DATA</a>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The <i>pNotify</i> parameter points to a structure that describes the volume change event that initiated the call to <b>OnNotify</b>. This structure contains an event-context GUID. This GUID enables a client to distinguish between a volume (or muting) change that it initiated and one that some other client initiated. When calling an <a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume</a> method that changes the volume level of the stream, a client passes in a pointer to an event-context GUID that its implementation of the <b>OnNotify</b> method can recognize. The structure pointed to by <i>pNotify</i> contains this context GUID. If the client that changes the volume level supplies a <b>NULL</b> pointer value for the pointer to the event-context GUID, the value of the event-context GUID in the structure pointed to by <i>pNotify</i> is GUID_NULL.

The Windows 7, the system's volume user interface does not specify GUID_NULL when it changes the volume in the system.   A third-party OSD application can differentiate between master volume control changes that result from the system's volume user interface, and other volume changes such as changes from the built-in volume control handler.

For a code example that implements the <b>OnNotify</b> method, see <a href="/windows/desktop/CoreAudio/endpoint-volume-controls">Endpoint Volume Controls</a>.

## -see-also

<a href="/windows/desktop/api/endpointvolume/ns-endpointvolume-audio_volume_notification_data">AUDIO_VOLUME_NOTIFICATION_DATA</a>



<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume Interface</a>



<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback Interface</a>