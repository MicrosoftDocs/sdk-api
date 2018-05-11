---
UID: NF:mmdeviceapi.IMMNotificationClient.OnDeviceRemoved
title: IMMNotificationClient::OnDeviceRemoved
author: windows-driver-content
description: The OnDeviceRemoved method indicates that an audio endpoint device has been removed.
old-location: coreaudio\immnotificationclient_ondeviceremoved.htm
old-project: CoreAudio
ms.assetid: 0adacdd2-5fa3-4d27-a299-fa0d41b6d285
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMMNotificationClient interface [Core Audio],OnDeviceRemoved method, IMMNotificationClient.OnDeviceRemoved, IMMNotificationClient::OnDeviceRemoved, IMMNotificationClientOnDeviceRemoved, OnDeviceRemoved, OnDeviceRemoved method [Core Audio], OnDeviceRemoved method [Core Audio],IMMNotificationClient interface, coreaudio.immnotificationclient_ondeviceremoved, mmdeviceapi/IMMNotificationClient::OnDeviceRemoved
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
req.typenames: EndpointFormFactor
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mmdeviceapi.h
api_name:
-	IMMNotificationClient.OnDeviceRemoved
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMMNotificationClient::OnDeviceRemoved


## -description



The <b>OnDeviceRemoved</b> method indicates that an audio endpoint device has been removed.




## -parameters




### -param pwstrDeviceId [in]

Pointer to the <a href="https://msdn.microsoft.com/3c955e2d-daaa-4b77-8ca5-890383bb2d39">endpoint ID string</a> that identifies the audio endpoint device. This parameter points to a null-terminated, wide-character string containing the endpoint ID. The string remains valid for the duration of the call.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



For a code example that implements the <b>OnDeviceRemoved</b> method, see <a href="https://msdn.microsoft.com/b31500d6-a79d-4e6e-878e-6bd77055f1ad">Device Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/76d3cd52-30bd-48b0-8adc-c23991a60d1b">IMMNotificationClient Interface</a>
 

 

