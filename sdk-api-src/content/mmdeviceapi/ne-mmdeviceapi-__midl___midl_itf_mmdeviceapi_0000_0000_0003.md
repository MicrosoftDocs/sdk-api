---
UID: NE:mmdeviceapi.__MIDL___MIDL_itf_mmdeviceapi_0000_0000_0003
title: "__MIDL___MIDL_itf_mmdeviceapi_0000_0000_0003"
author: windows-sdk-content
description: The EndpointFormFactor enumeration defines constants that indicate the general physical attributes of an audio endpoint device.
old-location: coreaudio\endpointformfactor.htm
old-project: CoreAudio
ms.assetid: 3fd3782b-c0fc-4d75-8627-d898e7fae436
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: DigitalAudioDisplayDevice, EndpointFormFactor, EndpointFormFactor , EndpointFormFactor enumeration [Core Audio], EndpointFormFactor_enum_count, Handset, Headphones, Headset, LineLevel, Microphone, RemoteNetworkDevice, SPDIF, Speakers, UnknownDigitalPassthrough, UnknownFormFactor, __MIDL___MIDL_itf_mmdeviceapi_0000_0000_0003, coreaudio.endpointformfactor, mmdeviceapi/DigitalAudioDisplayDevice, mmdeviceapi/EndpointFormFactor, mmdeviceapi/EndpointFormFactor_enum_count, mmdeviceapi/Handset, mmdeviceapi/Headphones, mmdeviceapi/Headset, mmdeviceapi/LineLevel, mmdeviceapi/Microphone, mmdeviceapi/RemoteNetworkDevice, mmdeviceapi/SPDIF, mmdeviceapi/Speakers, mmdeviceapi/UnknownDigitalPassthrough, mmdeviceapi/UnknownFormFactor
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: EndpointFormFactor
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmdeviceapi.h
api_name:
 - EndpointFormFactor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_mmdeviceapi_0000_0000_0003 enumeration


## -description



The <b>EndpointFormFactor</b> enumeration defines constants that indicate the general physical attributes of an audio endpoint device.




## -enum-fields




### -field RemoteNetworkDevice

An audio endpoint device that the user accesses remotely through a network.


### -field Speakers

A set of speakers.


### -field LineLevel

An audio endpoint device that sends a line-level analog signal to a line-input jack on an audio adapter or that receives a line-level analog signal from a line-output jack on the adapter.


### -field Headphones

A set of headphones.


### -field Microphone

A microphone.


### -field Headset

An earphone or a pair of earphones with an attached mouthpiece for two-way communication.


### -field Handset

The part of a telephone that is held in the hand and that contains a speaker and a microphone for two-way communication.


### -field UnknownDigitalPassthrough

An audio endpoint device that connects to an audio adapter through a connector for a digital interface of unknown type that transmits non-PCM data in digital pass-through mode. For more information, see Remarks.


### -field SPDIF

An audio endpoint device that connects to an audio adapter through a Sony/Philips Digital Interface (S/PDIF) connector.


### -field DigitalAudioDisplayDevice

An audio endpoint device that connects to an audio adapter through a High-Definition Multimedia Interface (HDMI) connector or a display port.

In <b>Windows Vista</b>, this value was named HDMI.


### -field UnknownFormFactor

An audio endpoint device with unknown physical attributes.


### -field EndpointFormFactor_enum_count

Windows 7: Maximum number of endpoint form factors.


## -remarks



The constants in this enumeration are the values that can be assigned to the <a href="https://msdn.microsoft.com/f49cb7da-3b50-47e2-90b4-1a885001b5d7">PKEY_AudioEndpoint_FormFactor</a> property.

In digital pass-through mode, a digital interface transports blocks of non-PCM data through a connection without modifying them and without attempting to interpret their contents. For more information about digital pass-through mode, see the following documentation:

<ul>
<li>The descriptions of the WAVE_FORMAT_WMA_SPDIF and WAVE_FORMAT_DOLBY_AC3_SPDIF wave-format tags in the Windows DDK documentation.</li>
<li>The white paper titled "Audio Driver Support for the WMA Pro-over-S/PDIF Format" at the <a href="http://go.microsoft.com/fwlink/p/?linkid=62989">Audio Device Technologies for Windows</a> website.</li>
</ul>
For information about obtaining a description of the audio jack or connector through which an audio endpoint device connects to an audio adapter, see <a href="https://msdn.microsoft.com/84278805-3b6d-4fae-8770-f9932b0e0fab">IKsJackDescription::GetJackDescription</a> and <a href="https://msdn.microsoft.com/724a75c2-22be-431c-b29a-8bf916d085e7">IKsJackDescription2::GetJackDescription2</a>. 




## -see-also




<a href="https://msdn.microsoft.com/7d25be71-ffbe-4e8c-9a45-cdeb35d10292">Core Audio Enumerations</a>



<a href="https://msdn.microsoft.com/84278805-3b6d-4fae-8770-f9932b0e0fab">IKsJackDescription::GetJackDescription</a>



<a href="https://msdn.microsoft.com/f49cb7da-3b50-47e2-90b4-1a885001b5d7">PKEY_AudioEndpoint_FormFactor Property</a>
 

 

