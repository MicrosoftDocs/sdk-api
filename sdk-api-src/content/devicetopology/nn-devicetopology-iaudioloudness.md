---
UID: NN:devicetopology.IAudioLoudness
title: IAudioLoudness
author: windows-sdk-content
description: The IAudioLoudness interface provides access to a &#0034;loudness&#0034; compensation control.
old-location: coreaudio\iaudioloudness.htm
tech.root: CoreAudio
ms.assetid: c182d6ae-c55b-4e3b-9639-7c2f2f7d826d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAudioLoudness, IAudioLoudness interface [Core Audio], IAudioLoudness interface [Core Audio],described, coreaudio.iaudioloudness, devicetopology/IAudioLoudness
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
 - IAudioLoudness
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioLoudness interface


## -description



The <b>IAudioLoudness</b> interface provides access to a "loudness" compensation control. The client obtains a reference to the <b>IAudioLoudness</b> interface of a subunit by calling the <a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioLoudness. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioLoudness</b> interface. Only a subunit object that represents a hardware loudness control function will support this interface.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioLoudness</b> interface provides convenient access to the KSPROPERTY_AUDIO_LOUDNESS property of a subunit that has a subtype GUID value of KSNODETYPE_LOUDNESS. To obtain the subtype GUID of a subunit, call the <a href="https://msdn.microsoft.com/456aaafb-1e68-4a3a-b27b-c6f6f89dc17b">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioLoudness</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioLoudness</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioLoudness</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ce0cd1b-e80f-45dc-b64e-1aa09bb53dbd">GetEnabled</a>
</td>
<td align="left" width="63%">
Gets the current state (enabled or disabled) of the loudness control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9102346-e853-40ae-ae10-a3e864ec5f17">SetEnabled</a>
</td>
<td align="left" width="63%">
Enables or disables the loudness control.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a>
 

 

