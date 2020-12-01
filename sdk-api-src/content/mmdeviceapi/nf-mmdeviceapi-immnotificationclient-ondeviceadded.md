---
UID: NF:mmdeviceapi.IMMNotificationClient.OnDeviceAdded
title: IMMNotificationClient::OnDeviceAdded (mmdeviceapi.h)
description: The OnDeviceAdded method indicates that a new audio endpoint device has been added.
helpviewer_keywords: ["IMMNotificationClient interface [Core Audio]","OnDeviceAdded method","IMMNotificationClient.OnDeviceAdded","IMMNotificationClient::OnDeviceAdded","IMMNotificationClientOnDeviceAdded","OnDeviceAdded","OnDeviceAdded method [Core Audio]","OnDeviceAdded method [Core Audio]","IMMNotificationClient interface","coreaudio.immnotificationclient_ondeviceadded","mmdeviceapi/IMMNotificationClient::OnDeviceAdded"]
old-location: coreaudio\immnotificationclient_ondeviceadded.htm
tech.root: CoreAudio
ms.assetid: c839493d-e53c-4afe-b53d-af9d1a6f2965
ms.date: 12/05/2018
ms.keywords: IMMNotificationClient interface [Core Audio],OnDeviceAdded method, IMMNotificationClient.OnDeviceAdded, IMMNotificationClient::OnDeviceAdded, IMMNotificationClientOnDeviceAdded, OnDeviceAdded, OnDeviceAdded method [Core Audio], OnDeviceAdded method [Core Audio],IMMNotificationClient interface, coreaudio.immnotificationclient_ondeviceadded, mmdeviceapi/IMMNotificationClient::OnDeviceAdded
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
 - IMMNotificationClient::OnDeviceAdded
 - mmdeviceapi/IMMNotificationClient::OnDeviceAdded
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
 - IMMNotificationClient.OnDeviceAdded
---

# IMMNotificationClient::OnDeviceAdded


## -description

The <b>OnDeviceAdded</b> method indicates that a new audio endpoint device has been added.

## -parameters

### -param pwstrDeviceId [in]

Pointer to the <a href="/windows/desktop/CoreAudio/endpoint-id-strings">endpoint ID string</a> that identifies the audio endpoint device. This parameter points to a null-terminated, wide-character string containing the endpoint ID. The string remains valid for the duration of the call.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

For a code example that implements the <b>OnDeviceAdded</b> method, see <a href="/windows/desktop/CoreAudio/device-events">Device Events</a>.

## -see-also

<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immnotificationclient">IMMNotificationClient Interface</a>