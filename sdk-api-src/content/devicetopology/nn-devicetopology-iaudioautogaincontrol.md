---
UID: NN:devicetopology.IAudioAutoGainControl
title: IAudioAutoGainControl
author: windows-sdk-content
description: The IAudioAutoGainControl interface provides access to a hardware automatic gain control (AGC).
old-location: coreaudio\iaudioautogaincontrol.htm
old-project: CoreAudio
ms.assetid: f21e27e6-f3a0-418a-ad2e-e3e104dd6da2
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IAudioAutoGainControl, IAudioAutoGainControl interface [Core Audio], IAudioAutoGainControl interface [Core Audio],described, coreaudio.iaudioautogaincontrol, devicetopology/IAudioAutoGainControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: devicetopology.h
req.include-header: 
req.redist: 
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
req.typenames: ConnectorType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IAudioAutoGainControl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioAutoGainControl interface


## -description



The <b>IAudioAutoGainControl</b> interface provides access to a hardware automatic gain control (AGC). The client obtains a reference to the <b>IAudioAutoGainControl</b> interface of a subunit by calling the <a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioAutoGainControl. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioAutoGainControl</b> interface. Only a subunit object that represents a hardware AGC function will support this interface.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioAutoGainControl</b> interface provides convenient access to the KSPROPERTY_AUDIO_AGC property of a subunit that has a subtype GUID value of KSNODETYPE_AGC. To obtain the subtype GUID of a subunit, call the <a href="https://msdn.microsoft.com/456aaafb-1e68-4a3a-b27b-c6f6f89dc17b">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioAutoGainControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioAutoGainControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioAutoGainControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9af85f6e-26b0-45bb-9694-a7578477b456">GetEnabled</a>
</td>
<td align="left" width="63%">
Gets the current state (enabled or disabled) of the AGC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05bf3b59-20e9-4bb0-931b-b6f28676cb5f">SetEnabled</a>
</td>
<td align="left" width="63%">
Enables or disables the AGC.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a>
 

 

