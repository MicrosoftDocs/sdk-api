---
UID: NN:devicetopology.IKsJackDescription2
title: IKsJackDescription2 (devicetopology.h)
author: windows-sdk-content
description: The IKsJackDescription2 interface provides information about the jacks or internal connectors that provide a physical connection between a device on an audio adapter and an external or internal endpoint device (for example, a microphone or CD player).
old-location: coreaudio\iksjackdescription2.htm
tech.root: CoreAudio
ms.assetid: 9a3d7631-6892-457a-91ab-484ae867fd9f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IKsJackDescription2, IKsJackDescription2 interface [Core Audio], IKsJackDescription2 interface [Core Audio],described, coreaudio.iksjackdescription2, devicetopology/IKsJackDescription2
ms.topic: interface
f1_keywords: 
 - "devicetopology/IKsJackDescription2"
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IKsJackDescription2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IKsJackDescription2 interface


## -description


The <b>IKsJackDescription2</b> interface provides information about the jacks or internal connectors that provide a physical connection between a device on an audio adapter and an external or internal endpoint device (for example, a microphone or CD player). 

In addition to getting jack information such as 
        type of connection, the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iksjackdescription">IKsJackDescription</a> is primarily used to report whether the jack was connected to the device. In  Windows 7, if the connected device driver supports <b>IKsJackDescription2</b>, the audio stack or an application can use this interface to get  information additional jack information. This includes the jack's detection capability and  if the format of the device has changed dynamically. 

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware description parameters in connectors (referred to as KS pins). The <b>IKsJackDescription2</b> interface provides convenient access to the <b>KSPROPERTY_JACK_DESCRIPTION2</b> property of a connector to an endpoint device. For more information about KS properties and KS pins, see the Windows DDK documentation.

An application obtains a reference to the <b>IKsJackDescription2</b> interface of a part by calling the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter <i>refiid</i> set to <b>REFIID</b><b>IID_IKsJackDescription2</b>. The call to <b>IPart::Activate</b> succeeds only if the part supports the <b>IKsJackDescription2</b> interface. Only a part object that represents a bridge pin connector on a KS filter device topology object supports this interface.

For a code example, see <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iksjackdescription">IKsJackDescription</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IKsJackDescription2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IKsJackDescription2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IKsJackDescription2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iksjackdescription2-getjackcount">GetJackCount</a>
</td>
<td align="left" width="63%">
Gets the number of jacks on the connector, which are required to connect to an endpoint device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2">GetJackDescription2</a>
</td>
<td align="left" width="63%">
Gets the description of a specified audio jack. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a>
 

 

