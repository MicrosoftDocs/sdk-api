---
UID: NF:mmdeviceapi.IMMNotificationClient.OnDeviceAdded
title: IMMNotificationClient::OnDeviceAdded
author: windows-sdk-content
description: The OnDeviceAdded method indicates that a new audio endpoint device has been added.
old-location: coreaudio\immnotificationclient_ondeviceadded.htm
tech.root: CoreAudio
ms.assetid: c839493d-e53c-4afe-b53d-af9d1a6f2965
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IMMNotificationClient interface [Core Audio],OnDeviceAdded method, IMMNotificationClient.OnDeviceAdded, IMMNotificationClient::OnDeviceAdded, IMMNotificationClientOnDeviceAdded, OnDeviceAdded, OnDeviceAdded method [Core Audio], OnDeviceAdded method [Core Audio],IMMNotificationClient interface, coreaudio.immnotificationclient_ondeviceadded, mmdeviceapi/IMMNotificationClient::OnDeviceAdded
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmdeviceapi.h
api_name:
 - IMMNotificationClient.OnDeviceAdded
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMMNotificationClient::OnDeviceAdded


## -description



The <b>OnDeviceAdded</b> method indicates that a new audio endpoint device has been added.




## -parameters




### -param pwstrDeviceId [in]

Pointer to the <a href="https://msdn.microsoft.com/3c955e2d-daaa-4b77-8ca5-890383bb2d39">endpoint ID string</a> that identifies the audio endpoint device. This parameter points to a null-terminated, wide-character string containing the endpoint ID. The string remains valid for the duration of the call.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



For a code example that implements the <b>OnDeviceAdded</b> method, see <a href="https://msdn.microsoft.com/b31500d6-a79d-4e6e-878e-6bd77055f1ad">Device Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/76d3cd52-30bd-48b0-8adc-c23991a60d1b">IMMNotificationClient Interface</a>
 

 

