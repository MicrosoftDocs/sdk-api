---
UID: NN:wsddisco.IWSDiscoveryProvider
title: IWSDiscoveryProvider
author: windows-sdk-content
description: Used to discover services on the network advertised by WS-Discovery.
old-location: ncd\iwsdiscoveryprovider.htm
old-project: WsdApi
ms.assetid: e3d3acc2-914b-40bd-9e1e-a3a612821ab7
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWSDiscoveryProvider, IWSDiscoveryProvider interface, IWSDiscoveryProvider interface,described, ncd.iwsdiscoveryprovider, wsddisco/IWSDiscoveryProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsddisco.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveryProvider
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDiscoveryProvider interface


## -description


This interface is used to discover services on the network advertised by WS-Discovery.

To get this interface, you can call <a href="https://msdn.microsoft.com/44275cbe-ea02-41fd-b88d-81d4df966067">WSDCreateDiscoveryProvider</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDiscoveryProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDiscoveryProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDiscoveryProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bb2aead-b082-4a2b-b4bf-97a1feb1e11e">Attach</a>
</td>
<td align="left" width="63%">
Attaches a callback interface to the discovery provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/562e7618-06ac-4bd3-9746-6ff3a7531b6b">Detach</a>
</td>
<td align="left" width="63%">
Detaches a callback interface from the discovery provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee2a862a-9d1d-4099-982e-259b6ab815f6">GetXMLContext</a>
</td>
<td align="left" width="63%">
Gets the  XML context associated with this provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64493841-0715-4bae-a416-aca9945b2420">SearchByAddress</a>
</td>
<td align="left" width="63%">
Initializes a search for WS-Discovery hosts by device address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78ae714a-1ee3-46eb-b3d6-ff46bf8974ab">SearchById</a>
</td>
<td align="left" width="63%">
Initializes a search for WS-Discovery hosts by device identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb1f2822-4d5d-4156-99e3-5a4528474953">SearchByType</a>
</td>
<td align="left" width="63%">
Initializes a search for WS-Discovery hosts by device type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33b13cd5-ea60-4928-a220-db563c00a43c">SetAddressFamily</a>
</td>
<td align="left" width="63%">
Specifies the IP address family (IPv4, IPv6, or both) to search when discovering WSD devices.

</td>
</tr>
</table> 


## -remarks



The Discovery Provider represents the "client" view of WS-Discovery.




## -see-also




<a href="https://msdn.microsoft.com/2b23d7d3-3b06-48c8-993e-49c72b139624">Overview of the WSDAPI Interfaces</a>
 

 

