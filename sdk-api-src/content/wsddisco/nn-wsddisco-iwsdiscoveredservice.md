---
UID: NN:wsddisco.IWSDiscoveredService
title: IWSDiscoveredService
author: windows-sdk-content
description: This interface represents a remotely discovered host.
old-location: ncd\iwsdiscoveredservice.htm
tech.root: WsdApi
ms.assetid: 6516098a-e440-4dec-b275-165ea3072d49
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWSDiscoveredService, IWSDiscoveredService interface, IWSDiscoveredService interface,described, ncd.iwsdiscoveredservice, wsddisco/IWSDiscoveredService
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# IWSDiscoveredService interface


## -description


This interface represents a remotely discovered host.  WSDAPI returns this interface when calling  <a href="https://msdn.microsoft.com/4e36157f-444d-4e59-bc30-c6def9c51cea">IWSDiscoveryProviderNotify::Add</a> and <a href="https://msdn.microsoft.com/776fc1d5-9dfe-445f-9af6-36faf971bf37">IWSDiscoveryProviderNotify::Remove</a>. The interface is populated when a match for an outstanding query issued using <a href="https://msdn.microsoft.com/bb1f2822-4d5d-4156-99e3-5a4528474953">IWSDiscoveryProvider::SearchByType</a>, <a href="https://msdn.microsoft.com/64493841-0715-4bae-a416-aca9945b2420">IWSDiscoveryProvider::SearchByAddress</a>, or <a href="https://msdn.microsoft.com/78ae714a-1ee3-46eb-b3d6-ff46bf8974ab">IWSDiscoveryProvider::SearchById</a> is received, or if a device on the network announces itself with a Hello message.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDiscoveredService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDiscoveredService</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/656ff77d-765e-4c30-8e5d-560d121dc368">GetEndpointReference</a>
</td>
<td align="left" width="63%">
Retrieves a WS-Addressing address referencing an endpoint of the remote device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ca12b1b-4adf-4c54-90b5-ab5286af9252">GetExtendedDiscoXML</a>
</td>
<td align="left" width="63%">
Retrieves custom or extensible data provided in the header or body of the SOAP message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/993f4ef1-ff13-4454-b22f-29c9628da5e0">GetInstanceId</a>
</td>
<td align="left" width="63%">
Retrieves the instance identifier of this message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c66bda4-d21c-443f-a9b0-e05485306bde">GetLocalInterfaceGUID</a>
</td>
<td align="left" width="63%">
Retrieves the GUID of the local network interface over which the message was received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7127ce7-175f-463e-8d54-0c637639a108">GetLocalTransportAddress</a>
</td>
<td align="left" width="63%">
Retrieves the string representation of the local transport (IP) address.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce0d463e-6455-48cc-b01f-6aa93fd628b6">GetMetadataVersion</a>
</td>
<td align="left" width="63%">
Retrieves the metadata version of this message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80c22d39-0197-4e4d-b47e-e04ae90716f9">GetProbeResolveTag</a>
</td>
<td align="left" width="63%">
Retrieves the search tag corresponding to this discovered service object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15376e12-fd7c-4cf5-a950-bf492392afa3">GetRemoteTransportAddress</a>
</td>
<td align="left" width="63%">
Retrieves the string representation of the remote transport (IP) address.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b389ba3-9cc1-4bc2-949a-e7103378cbcc">GetScopes</a>
</td>
<td align="left" width="63%">
Retrieves a list of WS-Discovery Scopes provided in the Hello, ProbeMatch, or ResolveMatch message sent by the remote device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fda4def4-4c1d-49a7-bfc1-56ff744a7a9d">GetTypes</a>
</td>
<td align="left" width="63%">
Retrieves a list of WS-Discovery Types provided in the Hello, ProbeMatch, or ResolveMatch message sent by the remote device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a861374e-fee4-486b-8e23-f4a4a8203b28">GetXAddrs</a>
</td>
<td align="left" width="63%">
Retrieves a list of WS-Discovery XAddrs provided in the Hello, ProbeMatch, or ResolveMatch message sent by the remote device.

</td>
</tr>
</table> 

