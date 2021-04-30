---
UID: NF:mmdeviceapi.IMMNotificationClient.OnDeviceRemoved
title: IMMNotificationClient::OnDeviceRemoved (mmdeviceapi.h)
description: The OnDeviceRemoved method indicates that an audio endpoint device has been removed.
helpviewer_keywords: ["IMMNotificationClient interface [Core Audio]","OnDeviceRemoved method","IMMNotificationClient.OnDeviceRemoved","IMMNotificationClient::OnDeviceRemoved","IMMNotificationClientOnDeviceRemoved","OnDeviceRemoved","OnDeviceRemoved method [Core Audio]","OnDeviceRemoved method [Core Audio]","IMMNotificationClient interface","coreaudio.immnotificationclient_ondeviceremoved","mmdeviceapi/IMMNotificationClient::OnDeviceRemoved"]
old-location: coreaudio\immnotificationclient_ondeviceremoved.htm
tech.root: CoreAudio
ms.assetid: 0adacdd2-5fa3-4d27-a299-fa0d41b6d285
ms.date: 12/05/2018
ms.keywords: IMMNotificationClient interface [Core Audio],OnDeviceRemoved method, IMMNotificationClient.OnDeviceRemoved, IMMNotificationClient::OnDeviceRemoved, IMMNotificationClientOnDeviceRemoved, OnDeviceRemoved, OnDeviceRemoved method [Core Audio], OnDeviceRemoved method [Core Audio],IMMNotificationClient interface, coreaudio.immnotificationclient_ondeviceremoved, mmdeviceapi/IMMNotificationClient::OnDeviceRemoved
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
 - IMMNotificationClient::OnDeviceRemoved
 - mmdeviceapi/IMMNotificationClient::OnDeviceRemoved
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
 - IMMNotificationClient.OnDeviceRemoved
---

# IMMNotificationClient::OnDeviceRemoved


## -description

The <b>OnDeviceRemoved</b> method indicates that an audio endpoint device has been removed.

## -parameters

### -param pwstrDeviceId [in]

Pointer to the <a href="/windows/desktop/CoreAudio/endpoint-id-strings">endpoint ID string</a> that identifies the audio endpoint device. This parameter points to a null-terminated, wide-character string containing the endpoint ID. The string remains valid for the duration of the call.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

For a code example that implements the <b>OnDeviceRemoved</b> method, see <a href="/windows/desktop/CoreAudio/device-events">Device Events</a>.

## -see-also

<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immnotificationclient">IMMNotificationClient Interface</a>