---
UID: NN:wsddisco.IWSDiscoveredService
title: IWSDiscoveredService (wsddisco.h)
author: windows-sdk-content
description: This interface represents a remotely discovered host.
old-location: ncd\iwsdiscoveredservice.htm
tech.root: WsdApi
ms.assetid: 6516098a-e440-4dec-b275-165ea3072d49
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDiscoveredService, IWSDiscoveredService interface, IWSDiscoveredService interface,described, ncd.iwsdiscoveredservice, wsddisco/IWSDiscoveredService
ms.topic: interface
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
 - IWSDiscoveredService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDiscoveredService interface


## -description


This interface represents a remotely discovered host.  WSDAPI returns this interface when calling  <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-add">IWSDiscoveryProviderNotify::Add</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-remove">IWSDiscoveryProviderNotify::Remove</a>. The interface is populated when a match for an outstanding query issued using <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype">IWSDiscoveryProvider::SearchByType</a>, <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress">IWSDiscoveryProvider::SearchByAddress</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid">IWSDiscoveryProvider::SearchById</a> is received, or if a device on the network announces itself with a Hello message.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDiscoveredService</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDiscoveredService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDiscoveredService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveredservice-getendpointreference">GetEndpointReference</a>
</td>
<td align="left" width="63%">
Retrieves a WS-Addressing address referencing an endpoint of the remote device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveredservice-getextendeddiscoxml">GetExtendedDiscoXML</a>
</td>
<td align="left" width="63%">
Retrieves custom or extensible data provided in the header or body of the SOAP message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveredservice-getinstanceid">GetInstanceId</a>
</td>
<td align="left" width="63%">
Retrieves the instance identifier of this message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveredservice-getlocalinterfaceguid">GetLocalInterfaceGUID</a>
</td>
<td align="left" width="63%">
Retrieves the GUID of the local network interface over which the message was received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveredservice-getlocaltransportaddress">GetLocalTransportAddress</a>
</td>
<td align="left" width="63%">
Retrieves the string representation of the local transport (IP) address.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveredservice-getmetadataversion">GetMetadataVersion</a>
</td>
<td align="left" width="63%">
Retrieves the metadata version of this message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveredservice-getproberesolvetag">GetProbeResolveTag</a>
</td>
<td align="left" width="63%">
Retrieves the search tag corresponding to this discovered service object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveredservice-getremotetransportaddress">GetRemoteTransportAddress</a>
</td>
<td align="left" width="63%">
Retrieves the string representation of the remote transport (IP) address.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveredservice-getscopes">GetScopes</a>
</td>
<td align="left" width="63%">
Retrieves a list of WS-Discovery Scopes provided in the Hello, ProbeMatch, or ResolveMatch message sent by the remote device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveredservice-gettypes">GetTypes</a>
</td>
<td align="left" width="63%">
Retrieves a list of WS-Discovery Types provided in the Hello, ProbeMatch, or ResolveMatch message sent by the remote device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveredservice-getxaddrs">GetXAddrs</a>
</td>
<td align="left" width="63%">
Retrieves a list of WS-Discovery XAddrs provided in the Hello, ProbeMatch, or ResolveMatch message sent by the remote device.

</td>
</tr>
</table> 

