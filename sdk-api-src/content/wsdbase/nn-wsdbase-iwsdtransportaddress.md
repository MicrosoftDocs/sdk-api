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

# IWSDTransportAddress interface


## -description


Represents an IP-based transport address.

You should not create an instance of the <b>IWSDTransportAddress</b> interface. Instead, create an instance of either the <a href="https://msdn.microsoft.com/79d3570a-56b2-40ad-b3c6-cddc3239da7e">IWSDHttpAddress</a> or <a href="https://msdn.microsoft.com/b666002f-2cd6-4e96-b055-34d801c1982e">IWSDUdpAddress</a> interface if an address object is required.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDTransportAddress</b> interface inherits from <a href="https://msdn.microsoft.com/b19938b2-2fba-42fe-8c4e-5696c40acd58">IWSDAddress</a>. <b>IWSDTransportAddress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDTransportAddress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc2e623f-e6b6-42ad-b0de-7960de0142d0">GetPort</a>
</td>
<td align="left" width="63%">
Gets the IP port number associated with this transport address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/090b009d-0cca-4925-bf90-cb3d0975d271">GetTransportAddress</a>
</td>
<td align="left" width="63%">
Gets a pointer to a string representation of the address object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b6f8e97-6387-4f2b-8388-775cc84e92f0">GetTransportAddressEx</a>
</td>
<td align="left" width="63%">
Gets a pointer to a string representation of the address object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0959e6f9-82cf-4634-9547-682df1965efa">SetPort</a>
</td>
<td align="left" width="63%">
Sets the IP port number for this transport address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea87b7d8-71c0-4cb6-b28b-7ac8f2417886">SetTransportAddress</a>
</td>
<td align="left" width="63%">
Sets the string representation of the transport address. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b19938b2-2fba-42fe-8c4e-5696c40acd58">IWSDAddress</a>
 

 

