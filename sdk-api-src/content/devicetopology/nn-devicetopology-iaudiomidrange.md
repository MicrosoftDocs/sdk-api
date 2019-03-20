---
UID: NN:devicetopology.IAudioMidrange
title: IAudioMidrange (devicetopology.h)
author: windows-sdk-content
description: The IAudioMidrange interface provides access to a hardware midrange-level control.
old-location: coreaudio\iaudiomidrange.htm
tech.root: CoreAudio
ms.assetid: d2d93dba-1867-4c3a-9cd1-60842bf8311d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAudioMidrange, IAudioMidrange interface [Core Audio], IAudioMidrange interface [Core Audio],described, coreaudio.iaudiomidrange, devicetopology/IAudioMidrange
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
 - IAudioMidrange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioMidrange interface


## -description



The <b>IAudioMidrange</b> interface provides access to a hardware midrange-level control. The client obtains a reference to the <b>IAudioMidrange</b> interface of a subunit by calling the <a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioMidrange. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioMidrange</b> interface. Only a subunit object that represents a hardware function for controlling the level of the mid-range frequencies in each channel will support this interface.

The <b>IAudioMidrange</b> interface provides per-channel controls for setting and getting the gain or attenuation level of the midrange frequencies in the audio stream. If a midrange-level hardware control can only attenuate the channels in the audio stream, then the maximum midrange level for any channel is 0 dB. If a midrange-level control can provide gain (amplification), then the maximum midrange level is greater than 0 dB.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioMidrange</b> interface provides convenient access to the KSPROPERTY_AUDIO_MID property of a subunit that has a subtype GUID value of KSNODETYPE_TONE. To obtain the subtype GUID of a subunit, call the <a href="https://msdn.microsoft.com/456aaafb-1e68-4a3a-b27b-c6f6f89dc17b">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a>



<a href="https://msdn.microsoft.com/e70b4518-c9de-4426-b8e5-db80656699a9">IPerChannelDbLevel Interface</a>
 

 

