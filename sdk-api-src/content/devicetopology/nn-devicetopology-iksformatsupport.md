---
UID: NN:devicetopology.IKsFormatSupport
title: IKsFormatSupport
author: windows-sdk-content
description: The IKsFormatSupport interface provides information about the audio data formats that are supported by a software-configured I/O connection (typically a DMA channel) between an audio adapter device and system memory.
old-location: coreaudio\iksformatsupport.htm
tech.root: CoreAudio
ms.assetid: 53a29b57-1650-4e4d-b9d2-95307063a733
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IKsFormatSupport, IKsFormatSupport interface [Core Audio], IKsFormatSupport interface [Core Audio],described, coreaudio.iksformatsupport, devicetopology/IKsFormatSupport
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
 - IKsFormatSupport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKsFormatSupport interface


## -description



The <b>IKsFormatSupport</b> interface provides information about the audio data formats that are supported by a software-configured I/O connection (typically a DMA channel) between an audio adapter device and system memory. The client obtains a reference to the <b>IKsFormatSupport</b> interface of a part by calling the <a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IKsFormatSupport. The call to <b>IPart::Activate</b> succeeds only if the part supports the <b>IKsFormatSupport</b> interface. Only a part object that represents a connector with a Software_IO connection type will support this interface. For more information about Software_IO, see <a href="https://msdn.microsoft.com/7171a880-2a3e-45aa-803d-26bf5e9e0365">ConnectorType Enumeration</a>.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware description parameters in connectors (referred to as KS pins). The <b>IKsFormatSupport</b> interface provides convenient access to the KSPROPERTY_PIN_DATAINTERSECTION and KSPROPERTY_PIN_PROPOSEDDATAFORMAT properties of a connector to a system bus (typically, PCI or PCI Express) or an external bus (for example, USB). Not all drivers support the KSPROPERTY_PIN_PROPOSEDDATAFORMAT property. If a driver does not support this property, <b>IKsFormatSupport</b> uses the information in the KS data ranges for the connector to determine whether the connector supports the proposed format. For more information about KS properties, KS pins, and KS data ranges, see the Windows DDK documentation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IKsFormatSupport</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IKsFormatSupport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IKsFormatSupport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a550ed25-020f-4d09-bfb4-76680539c50a">GetDevicePreferredFormat</a>
</td>
<td align="left" width="63%">
Gets the preferred audio stream format for the connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f377b14-fd19-40ac-9875-9ee3bd8d51c7">IsFormatSupported</a>
</td>
<td align="left" width="63%">
Indicates whether the audio adapter device supports the specified audio stream format.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a>
 

 

