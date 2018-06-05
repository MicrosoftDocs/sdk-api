---
UID: NF:mmdeviceapi.IMMNotificationClient.OnDeviceStateChanged
title: IMMNotificationClient::OnDeviceStateChanged
author: windows-sdk-content
description: The OnDeviceStateChanged method indicates that the state of an audio endpoint device has changed.
old-location: coreaudio\immnotificationclient_ondevicestatechanged.htm
old-project: CoreAudio
ms.assetid: 4725a300-c84b-40cd-93a6-6ef6c8e89708
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IMMNotificationClient interface [Core Audio],OnDeviceStateChanged method, IMMNotificationClient.OnDeviceStateChanged, IMMNotificationClient::OnDeviceStateChanged, IMMNotificationClientOnDeviceStateChanged, OnDeviceStateChanged, OnDeviceStateChanged method [Core Audio], OnDeviceStateChanged method [Core Audio],IMMNotificationClient interface, coreaudio.immnotificationclient_ondevicestatechanged, mmdeviceapi/IMMNotificationClient::OnDeviceStateChanged
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: EndpointFormFactor
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mmdeviceapi.h
api_name:
-	IMMNotificationClient.OnDeviceStateChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMMNotificationClient::OnDeviceStateChanged


## -description



The <b>OnDeviceStateChanged</b> method indicates that the state of an audio endpoint device has changed.




## -parameters




### -param pwstrDeviceId [in]

Pointer to the <a href="https://msdn.microsoft.com/3c955e2d-daaa-4b77-8ca5-890383bb2d39">endpoint ID string</a> that identifies the audio endpoint device. This parameter points to a null-terminated, wide-character string containing the endpoint ID. The string remains valid for the duration of the call.


### -param dwNewState [in]

Specifies the new state of the endpoint device. The value of this parameter is one of the following <a href="https://msdn.microsoft.com/d03f2fbc-313a-42cf-902a-fd9f6dce2a35">DEVICE_STATE_XXX</a> constants:

DEVICE_STATE_ACTIVE

DEVICE_STATE_DISABLED

DEVICE_STATE_NOTPRESENT

DEVICE_STATE_UNPLUGGED


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



For a code example that implements the <b>OnDeviceStateChanged</b> method, see <a href="https://msdn.microsoft.com/b31500d6-a79d-4e6e-878e-6bd77055f1ad">Device Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/76d3cd52-30bd-48b0-8adc-c23991a60d1b">IMMNotificationClient Interface</a>
 

 

