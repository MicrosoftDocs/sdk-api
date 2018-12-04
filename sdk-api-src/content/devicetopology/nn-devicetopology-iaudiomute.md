---
UID: NN:devicetopology.IAudioMute
title: IAudioMute
author: windows-sdk-content
description: The IAudioMute interface provides access to a hardware mute control.
old-location: coreaudio\iaudiomute.htm
tech.root: CoreAudio
ms.assetid: 53d49af7-81c3-4e75-ba06-dcee34d84292
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IAudioMute, IAudioMute interface [Core Audio], IAudioMute interface [Core Audio],described, coreaudio.iaudiomute, devicetopology/IAudioMute
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
 - IAudioMute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioMute interface


## -description



The <b>IAudioMute</b> interface provides access to a hardware mute control. The client obtains a reference to the <b>IAudioMute</b> interface of a subunit by calling the <a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioMute. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioMute</b> interface. Only a subunit object that represents a hardware mute control function will support this interface.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioMute</b> interface provides convenient access to the KSPROPERTY_AUDIO_MUTE property of a subunit that has a subtype GUID value of KSNODETYPE_MUTE. To obtain the subtype GUID of a subunit, call the <a href="https://msdn.microsoft.com/456aaafb-1e68-4a3a-b27b-c6f6f89dc17b">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioMute</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioMute</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioMute</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b6421d3-f238-46f6-a74a-085a63bf5441">GetMute</a>
</td>
<td align="left" width="63%">
Gets the current state (enabled or disabled) of the mute control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e99cb894-b39e-42ec-be8f-dc3fa6e7abcd">SetMute</a>
</td>
<td align="left" width="63%">
Enables or disables the mute control.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a>
 

 

