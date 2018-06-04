---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IKsJackDescription2 interface


## -description


The <b>IKsJackDescription2</b> interface provides information about the jacks or internal connectors that provide a physical connection between a device on an audio adapter and an external or internal endpoint device (for example, a microphone or CD player). 

In addition to getting jack information such as 
        type of connection, the <a href="https://msdn.microsoft.com/0ca9e719-7179-4302-99ff-df137141f58f">IKsJackDescription</a> is primarily used to report whether the jack was connected to the device. In  Windows 7, if the connected device driver supports <b>IKsJackDescription2</b>, the audio stack or an application can use this interface to get  information additional jack information. This includes the jack's detection capability and  if the format of the device has changed dynamically. 

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware description parameters in connectors (referred to as KS pins). The <b>IKsJackDescription2</b> interface provides convenient access to the <b>KSPROPERTY_JACK_DESCRIPTION2</b> property of a connector to an endpoint device. For more information about KS properties and KS pins, see the Windows DDK documentation.

An application obtains a reference to the <b>IKsJackDescription2</b> interface of a part by calling the <a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a> method with parameter <i>refiid</i> set to <b>REFIID</b><b>IID_IKsJackDescription2</b>. The call to <b>IPart::Activate</b> succeeds only if the part supports the <b>IKsJackDescription2</b> interface. Only a part object that represents a bridge pin connector on a KS filter device topology object supports this interface.

For a code example, see <a href="https://msdn.microsoft.com/0ca9e719-7179-4302-99ff-df137141f58f">IKsJackDescription</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IKsJackDescription2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IKsJackDescription2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b7ebe746-4680-4921-a1fd-1940e306f4eb">GetJackCount</a>
</td>
<td align="left" width="63%">
Gets the number of jacks on the connector, which are required to connect to an endpoint device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/724a75c2-22be-431c-b29a-8bf916d085e7">GetJackDescription2</a>
</td>
<td align="left" width="63%">
Gets the description of a specified audio jack. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a>
 

 

