---
UID: NN:devicetopology.IAudioVolumeLevel
title: IAudioVolumeLevel
author: windows-sdk-content
description: The IAudioVolumeLevel interface provides access to a hardware volume control.
old-location: coreaudio\iaudiovolumelevel.htm
tech.root: CoreAudio
ms.assetid: 5e7d7111-e4b0-43b3-af35-9878d1a19e5f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAudioVolumeLevel, IAudioVolumeLevel interface [Core Audio], IAudioVolumeLevel interface [Core Audio],described, coreaudio.iaudiovolumelevel, devicetopology/IAudioVolumeLevel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: devicetopology.h
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
 - Devicetopology.h
api_name:
 - IAudioVolumeLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioVolumeLevel interface


## -description



The <b>IAudioVolumeLevel</b> interface provides access to a hardware volume control. The client obtains a reference to the <b>IAudioVolumeLevel</b> interface of a subunit by calling the <a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioVolumeLevel. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioVolumeLevel</b> interface. Only a subunit object that represents a hardware volume-level control will support this interface.



The <b>IAudioVolumeLevel</b> interface provides per-channel controls for setting and getting the gain or attenuation levels in an the audio stream. If a volume-level hardware control can only attenuate the channels in the audio stream, then the maximum volume level for any channel is 0 dB. If a volume-level control can provide gain (amplification), then the maximum volume level is greater than 0 dB.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioVolumeLevel</b> interface provides convenient access to the KSPROPERTY_AUDIO_VOLUMELEVEL property of a subunit that has a subtype GUID value of KSNODETYPE_VOLUME. To obtain the subtype GUID of a subunit, call the <a href="https://msdn.microsoft.com/456aaafb-1e68-4a3a-b27b-c6f6f89dc17b">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a>



<a href="https://msdn.microsoft.com/e70b4518-c9de-4426-b8e5-db80656699a9">IPerChannelDbLevel Interface</a>
 

 

