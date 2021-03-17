---
UID: NF:mmdeviceapi.IMMNotificationClient.OnDeviceStateChanged
title: IMMNotificationClient::OnDeviceStateChanged (mmdeviceapi.h)
description: The OnDeviceStateChanged method indicates that the state of an audio endpoint device has changed.
helpviewer_keywords: ["IMMNotificationClient interface [Core Audio]","OnDeviceStateChanged method","IMMNotificationClient.OnDeviceStateChanged","IMMNotificationClient::OnDeviceStateChanged","IMMNotificationClientOnDeviceStateChanged","OnDeviceStateChanged","OnDeviceStateChanged method [Core Audio]","OnDeviceStateChanged method [Core Audio]","IMMNotificationClient interface","coreaudio.immnotificationclient_ondevicestatechanged","mmdeviceapi/IMMNotificationClient::OnDeviceStateChanged"]
old-location: coreaudio\immnotificationclient_ondevicestatechanged.htm
tech.root: CoreAudio
ms.assetid: 4725a300-c84b-40cd-93a6-6ef6c8e89708
ms.date: 12/05/2018
ms.keywords: IMMNotificationClient interface [Core Audio],OnDeviceStateChanged method, IMMNotificationClient.OnDeviceStateChanged, IMMNotificationClient::OnDeviceStateChanged, IMMNotificationClientOnDeviceStateChanged, OnDeviceStateChanged, OnDeviceStateChanged method [Core Audio], OnDeviceStateChanged method [Core Audio],IMMNotificationClient interface, coreaudio.immnotificationclient_ondevicestatechanged, mmdeviceapi/IMMNotificationClient::OnDeviceStateChanged
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
 - IMMNotificationClient::OnDeviceStateChanged
 - mmdeviceapi/IMMNotificationClient::OnDeviceStateChanged
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
 - IMMNotificationClient.OnDeviceStateChanged
---

# IMMNotificationClient::OnDeviceStateChanged


## -description

The <b>OnDeviceStateChanged</b> method indicates that the state of an audio endpoint device has changed.

## -parameters

### -param pwstrDeviceId [in]

Pointer to the <a href="/windows/desktop/CoreAudio/endpoint-id-strings">endpoint ID string</a> that identifies the audio endpoint device. This parameter points to a null-terminated, wide-character string containing the endpoint ID. The string remains valid for the duration of the call.

### -param dwNewState [in]

Specifies the new state of the endpoint device. The value of this parameter is one of the following <a href="/windows/desktop/CoreAudio/device-state-xxx-constants">DEVICE_STATE_XXX</a> constants:

DEVICE_STATE_ACTIVE

DEVICE_STATE_DISABLED

DEVICE_STATE_NOTPRESENT

DEVICE_STATE_UNPLUGGED

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

For a code example that implements the <b>OnDeviceStateChanged</b> method, see <a href="/windows/desktop/CoreAudio/device-events">Device Events</a>.

## -see-also

<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immnotificationclient">IMMNotificationClient Interface</a>