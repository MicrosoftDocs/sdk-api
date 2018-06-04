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

# IWSDUdpMessageParameters interface


## -description


Use this interface to specify how often WSD repeats the message transmission.

To get this interface from a UDP message sent during discovery, call the  <b>QueryInterface</b> method of <a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a> passing __uuidof(IWSDUdpMessageParameters) as the interface identifier.

You can also call <a href="https://msdn.microsoft.com/a183a5f8-edd9-4881-84d4-b23701c40f36">WSDCreateUdpMessageParameters</a> to retrieve this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDUdpMessageParameters</b> interface inherits from <a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a>. <b>IWSDUdpMessageParameters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDUdpMessageParameters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c34d6320-c70b-410e-ae21-fba849dac62f">GetRetransmitParams</a>
</td>
<td align="left" width="63%">
Retrieves the values that WSD uses to determine how often to repeat the message transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8fef8dc9-7621-4928-94a6-491a095b11fa">SetRetransmitParams</a>
</td>
<td align="left" width="63%">
Sets the values that WSD uses to determine how often to repeat the message transmission.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a>
 

 

