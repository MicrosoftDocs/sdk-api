---
UID: NF:mmdeviceapi.IMMNotificationClient.OnDefaultDeviceChanged
title: IMMNotificationClient::OnDefaultDeviceChanged (mmdeviceapi.h)
description: The OnDefaultDeviceChanged method notifies the client that the default audio endpoint device for a particular device role has changed.
helpviewer_keywords: ["IMMNotificationClient interface [Core Audio]","OnDefaultDeviceChanged method","IMMNotificationClient.OnDefaultDeviceChanged","IMMNotificationClient::OnDefaultDeviceChanged","IMMNotificationClientOnDefaultDeviceChanged","OnDefaultDeviceChanged","OnDefaultDeviceChanged method [Core Audio]","OnDefaultDeviceChanged method [Core Audio]","IMMNotificationClient interface","coreaudio.immnotificationclient_ondefaultdevicechanged","mmdeviceapi/IMMNotificationClient::OnDefaultDeviceChanged"]
old-location: coreaudio\immnotificationclient_ondefaultdevicechanged.htm
tech.root: CoreAudio
ms.assetid: 3d484e5d-bdc6-41f1-bd94-ab0c9e109222
ms.date: 12/05/2018
ms.keywords: IMMNotificationClient interface [Core Audio],OnDefaultDeviceChanged method, IMMNotificationClient.OnDefaultDeviceChanged, IMMNotificationClient::OnDefaultDeviceChanged, IMMNotificationClientOnDefaultDeviceChanged, OnDefaultDeviceChanged, OnDefaultDeviceChanged method [Core Audio], OnDefaultDeviceChanged method [Core Audio],IMMNotificationClient interface, coreaudio.immnotificationclient_ondefaultdevicechanged, mmdeviceapi/IMMNotificationClient::OnDefaultDeviceChanged
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
 - IMMNotificationClient::OnDefaultDeviceChanged
 - mmdeviceapi/IMMNotificationClient::OnDefaultDeviceChanged
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
 - IMMNotificationClient.OnDefaultDeviceChanged
---

# IMMNotificationClient::OnDefaultDeviceChanged


## -description

The <b>OnDefaultDeviceChanged</b> method notifies the client that the default audio endpoint device for a particular <a href="/windows/desktop/CoreAudio/device-roles">device role</a> has changed.

## -parameters

### -param flow [in]

The data-flow direction of the endpoint device. This parameter is set to one of the following <a href="/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow">EDataFlow</a> enumeration values:

eRender

eCapture

The data-flow direction for a rendering device is eRender. The data-flow direction for a capture device is eCapture.

### -param role [in]

The <a href="/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole">device role</a> of the audio endpoint device. This parameter is set to one of the following <a href="/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole">ERole</a> enumeration values:

eConsole

eMultimedia

eCommunications

### -param pwstrDefaultDeviceId [in]

Pointer to the <a href="/windows/desktop/CoreAudio/endpoint-id-strings">endpoint ID string</a> that identifies the audio endpoint device. This parameter points to a null-terminated, wide-character string containing the endpoint ID. The string remains valid for the duration of the call. If the user has removed or disabled the default device for a particular role, and no other device is available to assume that role, then <i>pwstrDefaultDevice</i> is <b>NULL</b>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The three input parameters specify the data-flow direction, device role, and endpoint ID string of the new default audio endpoint device.

In Windows Vista, the MMDevice API supports device roles but the system-supplied user interface programs do not. The user interface in Windows Vista enables the user to select a default audio device for rendering and a default audio device for capture. When the user changes the default rendering or capture device, the system assigns all three device roles (eConsole, eMultimedia, and eCommunications) to the new device. Thus, when the user changes the default rendering or capture device, the system calls the client's <b>OnDefaultDeviceChanged</b> method three times—once for each of the three device roles.

In a future version of Windows, the user interface might enable the user to assign individual roles to different devices. In that case, if the user changes the assignment of only one or two device roles to a new rendering or capture device, the system will call the client's <b>OnDefaultDeviceChanged</b> method only once or twice (that is, one call per changed role). Depending on how the <b>OnDefaultDeviceChanged</b> method responds to role changes, the behavior of an audio application developed to run in Windows Vista might change when run in a future version of Windows. For more information, see <a href="/windows/desktop/CoreAudio/device-roles-in-windows-vista">Device Roles in Windows Vista</a>.

For a code example that implements the <b>OnDefaultDeviceChanged</b> method, see <a href="/windows/desktop/CoreAudio/device-events">Device Events</a>.

## -see-also

<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immnotificationclient">IMMNotificationClient Interface</a>