---
UID: NE:mmdeviceapi.__MIDL___MIDL_itf_mmdeviceapi_0000_0000_0001
title: "__MIDL___MIDL_itf_mmdeviceapi_0000_0000_0001"
author: windows-sdk-content
description: The EDataFlow enumeration defines constants that indicate the direction in which audio data flows between an audio endpoint device and an application.
old-location: coreaudio\edataflow.htm
tech.root: CoreAudio
ms.assetid: d79315aa-d753-4674-84c2-9ba601f36f57
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EDataFlow, EDataFlow , EDataFlow enumeration [Core Audio], EDataFlow_enum_count, __MIDL___MIDL_itf_mmdeviceapi_0000_0000_0001, coreaudio.edataflow, eAll, eCapture, eRender, mmdeviceapi/EDataFlow, mmdeviceapi/EDataFlow_enum_count, mmdeviceapi/eAll, mmdeviceapi/eCapture, mmdeviceapi/eRender
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - HeaderDef
api_location:
 - Mmdeviceapi.h
api_name:
 - EDataFlow
product: Windows
targetos: Windows
req.typenames: EDataFlow
req.redist: 
---

# __MIDL___MIDL_itf_mmdeviceapi_0000_0000_0001 enumeration


## -description



The <b>EDataFlow</b> enumeration defines constants that indicate the direction in which audio data flows between an audio endpoint device and an application.




## -enum-fields




### -field eRender

Audio rendering stream. Audio data flows from the application to the audio endpoint device, which renders the stream.


### -field eCapture

Audio capture stream. Audio data flows from the audio endpoint device that captures the stream, to the application.


### -field eAll

Audio rendering or capture stream. Audio data can flow either from the application to the audio endpoint device, or from the audio endpoint device to the application.


### -field EDataFlow_enum_count

The number of members in the <a href="https://msdn.microsoft.com/d79315aa-d753-4674-84c2-9ba601f36f57">EDataFlow</a> enumeration (not counting the EDataFlow_enum_count member).


## -remarks



The <a href="https://msdn.microsoft.com/96776d2a-27b7-490a-b3a8-04782ec34f91">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a>, <a href="https://msdn.microsoft.com/ebdd2dcd-82c5-423f-a85d-04388f5078ec">IMMDeviceEnumerator::EnumAudioEndpoints</a>, <a href="https://msdn.microsoft.com/01882c44-bf0c-4180-846e-c1e98c6fb472">IMMEndpoint::GetDataFlow</a>, and <a href="https://msdn.microsoft.com/3d484e5d-bdc6-41f1-bd94-ab0c9e109222">IMMNotificationClient::OnDefaultDeviceChanged</a> methods use the constants defined in the <b>EDataFlow</b> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/7d25be71-ffbe-4e8c-9a45-cdeb35d10292">Core Audio Enumerations</a>



<a href="https://msdn.microsoft.com/ebdd2dcd-82c5-423f-a85d-04388f5078ec">IMMDeviceEnumerator::EnumAudioEndpoints</a>



<a href="https://msdn.microsoft.com/96776d2a-27b7-490a-b3a8-04782ec34f91">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a>



<a href="https://msdn.microsoft.com/01882c44-bf0c-4180-846e-c1e98c6fb472">IMMEndpoint::GetDataFlow</a>



<a href="https://msdn.microsoft.com/3d484e5d-bdc6-41f1-bd94-ab0c9e109222">IMMNotificationClient::OnDefaultDeviceChanged</a>
 

 

