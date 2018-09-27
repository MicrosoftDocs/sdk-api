---
UID: NN:devicetopology.IAudioChannelConfig
title: IAudioChannelConfig
author: windows-sdk-content
description: The IAudioChannelConfig interface provides access to a hardware channel-configuration control.
old-location: coreaudio\iaudiochannelconfig.htm
tech.root: CoreAudio
ms.assetid: b8e54e9e-a6eb-46e6-a71c-ff498c7e8f47
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAudioChannelConfig, IAudioChannelConfig interface [Core Audio], IAudioChannelConfig interface [Core Audio],described, coreaudio.iaudiochannelconfig, devicetopology/IAudioChannelConfig
ms.prod: windows
ms.technology: windows-sdk
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
 - IAudioChannelConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioChannelConfig interface


## -description



The <b>IAudioChannelConfig</b> interface provides access to a hardware channel-configuration control. The client obtains a reference to the <b>IAudioChannelConfig</b> interface of a subunit by calling the <a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioChannelConfig. The call to IPart::Activate succeeds only if the subunit supports the <b>IAudioChannelConfig</b> interface. Only a subunit object that represents a hardware channel-configuration control will support this interface.

A client of the <b>IAudioChannelConfig</b> interface programs a hardware channel-configuration control by writing a channel-configuration mask to the control. The mask specifies the assignment of audio channels to speakers. For more information about channel-configuration masks, see the following:

<ul>
<li>The discussion of the KSPROPERTY_AUDIO_CHANNEL_CONFIG property in the Windows DDK documentation.</li>
<li>The white paper titled "Audio Driver Support for Home Theater Speaker Configurations" at the <a href="http://go.microsoft.com/fwlink/p/?linkid=62989">Audio Device Technologies for Windows</a> website.</li>
</ul>
Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioChannelConfig</b> interface provides convenient access to the KSPROPERTY_AUDIO_CHANNEL_CONFIG property of a subunit that has a subtype GUID value of KSNODETYPE_3D_EFFECTS, KSNODETYPE_DAC, KSNODETYPE_VOLUME, or KSNODETYPE_PROLOGIC_DECODER. To obtain the subtype GUID of a subunit, call the <a href="https://msdn.microsoft.com/456aaafb-1e68-4a3a-b27b-c6f6f89dc17b">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioChannelConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioChannelConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioChannelConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91331c34-9805-424b-b2c9-5705a11c594d">GetChannelConfig</a>
</td>
<td align="left" width="63%">
Gets the current channel-configuration mask from a channel-configuration control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a63b92ab-8abf-4582-b408-6c3e94a6bd3c">SetChannelConfig</a>
</td>
<td align="left" width="63%">
Sets the channel-configuration mask in a channel-configuration control.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a>
 

 

