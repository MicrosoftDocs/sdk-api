---
UID: NN:wsddisco.IWSDiscoveryProvider
title: IWSDiscoveryProvider (wsddisco.h)
author: windows-sdk-content
description: Used to discover services on the network advertised by WS-Discovery.
old-location: ncd\iwsdiscoveryprovider.htm
tech.root: WsdApi
ms.assetid: e3d3acc2-914b-40bd-9e1e-a3a612821ab7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryProvider, IWSDiscoveryProvider interface, IWSDiscoveryProvider interface,described, ncd.iwsdiscoveryprovider, wsddisco/IWSDiscoveryProvider
ms.topic: interface
f1_keywords: 
 - "wsddisco/IWSDiscoveryProvider"
req.header: wsddisco.h
req.include-header: Wsdapi.h
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
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDiscoveryProvider interface


## -description


This interface is used to discover services on the network advertised by WS-Discovery.

To get this interface, you can call <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-wsdcreatediscoveryprovider">WSDCreateDiscoveryProvider</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDiscoveryProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDiscoveryProvider</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-attach">Attach</a>
</td>
<td align="left" width="63%">
Attaches a callback interface to the discovery provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-detach">Detach</a>
</td>
<td align="left" width="63%">
Detaches a callback interface from the discovery provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-getxmlcontext">GetXMLContext</a>
</td>
<td align="left" width="63%">
Gets the  XML context associated with this provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress">SearchByAddress</a>
</td>
<td align="left" width="63%">
Initializes a search for WS-Discovery hosts by device address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid">SearchById</a>
</td>
<td align="left" width="63%">
Initializes a search for WS-Discovery hosts by device identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype">SearchByType</a>
</td>
<td align="left" width="63%">
Initializes a search for WS-Discovery hosts by device type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-setaddressfamily">SetAddressFamily</a>
</td>
<td align="left" width="63%">
Specifies the IP address family (IPv4, IPv6, or both) to search when discovering WSD devices.

</td>
</tr>
</table> 


## -remarks



The Discovery Provider represents the "client" view of WS-Discovery.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WsdApi/overview-of-the-wsdapi-interfaces">Overview of the WSDAPI Interfaces</a>
 

 

