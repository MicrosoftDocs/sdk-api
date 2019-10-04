---
UID: NE:mmdeviceapi.__MIDL___MIDL_itf_mmdeviceapi_0000_0000_0001
title: EDataFlow (mmdeviceapi.h)
author: windows-sdk-content
description: The EDataFlow enumeration defines constants that indicate the direction in which audio data flows between an audio endpoint device and an application.
old-location: coreaudio\edataflow.htm
tech.root: CoreAudio
ms.assetid: d79315aa-d753-4674-84c2-9ba601f36f57
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EDataFlow, EDataFlow , EDataFlow enumeration [Core Audio], EDataFlow_enum_count, coreaudio.edataflow, eAll, eCapture, eRender, mmdeviceapi/EDataFlow, mmdeviceapi/EDataFlow_enum_count, mmdeviceapi/eAll, mmdeviceapi/eCapture, mmdeviceapi/eRender
ms.topic: enum
f1_keywords: 
 - "mmdeviceapi/EDataFlow"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: EDataFlow
req.redist: 
ms.custom: 19H1
---

# EDataFlow enumeration


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

The number of members in the <a href="https://docs.microsoft.com/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow">EDataFlow</a> enumeration (not counting the EDataFlow_enum_count member).


## -remarks



The <a href="https://docs.microsoft.com/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a>, <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints">IMMDeviceEnumerator::EnumAudioEndpoints</a>, <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immendpoint-getdataflow">IMMEndpoint::GetDataFlow</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged">IMMNotificationClient::OnDefaultDeviceChanged</a> methods use the constants defined in the <b>EDataFlow</b> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-enumerations">Core Audio Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints">IMMDeviceEnumerator::EnumAudioEndpoints</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immendpoint-getdataflow">IMMEndpoint::GetDataFlow</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged">IMMNotificationClient::OnDefaultDeviceChanged</a>
 

 

