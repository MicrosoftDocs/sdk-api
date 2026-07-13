---
UID: NN:mmdeviceapi.IMMNotificationClient
title: IMMNotificationClient (mmdeviceapi.h)
description: The IMMNotificationClient interface provides notifications when an audio endpoint device is added or removed, when the state or properties of an endpoint device change, or when there is a change in the default role assigned to an endpoint device.
helpviewer_keywords: ["IMMNotificationClient","IMMNotificationClient interface [Core Audio]","IMMNotificationClient interface [Core Audio]","described","coreaudio.immnotificationclient","mmdeviceapi/IMMNotificationClient"]
old-location: coreaudio\immnotificationclient.htm
tech.root: CoreAudio
ms.assetid: 76d3cd52-30bd-48b0-8adc-c23991a60d1b
ms.date: 12/05/2018
ms.keywords: IMMNotificationClient, IMMNotificationClient interface [Core Audio], IMMNotificationClient interface [Core Audio],described, coreaudio.immnotificationclient, mmdeviceapi/IMMNotificationClient
req.header: mmdeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMMNotificationClient
 - mmdeviceapi/IMMNotificationClient
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmdeviceapi.h
api_name:
 - IMMNotificationClient
---

# IMMNotificationClient interface


## -description

The <b>IMMNotificationClient</b> interface provides notifications when an <a href="/windows/desktop/CoreAudio/audio-endpoint-devices">audio endpoint device</a> is added or removed, when the state or properties of an endpoint device change, or when there is a change in the default role assigned to an endpoint device. Unlike the other interfaces in this section, which are implemented by the MMDevice API system component, an MMDevice API client implements the <b>IMMNotificationClient</b> interface. To receive notifications, the client passes a pointer to its <b>IMMNotificationClient</b> interface instance as a parameter to the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback">IMMDeviceEnumerator::RegisterEndpointNotificationCallback</a> method.

After registering its <b>IMMNotificationClient</b> interface, the client receives event notifications in the form of callbacks through the methods of the interface.

Each method in the <b>IMMNotificationClient</b> interface receives, as one of its input parameters, an <a href="/windows/desktop/CoreAudio/endpoint-id-strings">endpoint ID string</a> that identifies the audio endpoint device that is the subject of the notification. The string uniquely identifies the device with respect to all of the other audio endpoint devices in the system. The methods in the <b>IMMNotificationClient</b> interface implementation should treat this string as opaque. That is, none of the methods should attempt to parse the contents of the string to obtain information about the device. The reason is that the string format is undefined and might change from one implementation of the MMDevice API system module to the next.

A client can use the endpoint ID string that it receives as an input parameter in a call to an <b>IMMNotificationClient</b> method in two ways:

<ul>
<li>The client can create an instance of the device that the endpoint ID string identifies. The client does this by calling the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice">IMMDeviceEnumerator::GetDevice</a> method and supplying the endpoint ID string as an input parameter.</li>
<li>The client can compare the endpoint ID string with the endpoint ID string of an existing device instance. To obtain the second endpoint ID string, the client calls the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid">IMMDevice::GetId</a> method of the device instance. If the two strings match, they identify the same device.</li>
</ul>
In implementing the <b>IMMNotificationClient</b> interface, the client should observe these rules to avoid deadlocks and undefined behavior:

<ul>
<li>The methods of the interface must be nonblocking. The client should never wait on a synchronization object during an event callback.</li>
<li>To avoid dead locks, the client should never call <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback">IMMDeviceEnumerator::RegisterEndpointNotificationCallback</a> or <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback">IMMDeviceEnumerator::UnregisterEndpointNotificationCallback</a> in its implementation of  <b>IMMNotificationClient</b> methods. </li>
<li>The client should never release the final reference on an MMDevice API object during an event callback.</li>
</ul>
For a code example that implements the <b>IMMNotificationClient</b> interface, see <a href="/windows/desktop/CoreAudio/device-events">Device Events</a>.

## -inheritance

The <b>IMMNotificationClient</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMMNotificationClient</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid">IMMDevice::GetId</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice">IMMDeviceEnumerator::GetDevice</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback">IMMDeviceEnumerator::RegisterEndpointNotificationCallback</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback">IMMDeviceEnumerator::UnregisterEndpointNotificationCallback</a>



<a href="/windows/desktop/CoreAudio/mmdevice-api">MMDevice API</a>
