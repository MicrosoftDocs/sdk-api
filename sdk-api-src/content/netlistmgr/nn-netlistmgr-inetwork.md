---
UID: NN:netlistmgr.INetwork
title: INetwork (netlistmgr.h)
author: windows-sdk-content
description: The INetwork interface represents a network on the local machine. It can also represent a collection of network connections with a similar network signature.
old-location: nla\inetwork.htm
tech.root: nla
ms.assetid: 6d483058-f7c4-4a6c-a1a8-816c2fab9994
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INetwork, INetwork interface [Network Awareness], INetwork interface [Network Awareness],described, netlistmgr/INetwork, nla.inetwork
ms.topic: interface
f1_keywords: ["netlistmgr/INetwork"]
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Netlistmgr.idl
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
 - Netlistmgr.h
api_name:
 - INetwork
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetwork interface


## -description


The <b>INetwork</b> interface represents a network on the local machine. It can also represent a collection of network connections with a similar network signature.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetwork</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INetwork</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetwork</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetwork-getcategory">GetCategory</a>
</td>
<td align="left" width="63%">
Returns the category of a network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetwork-getconnectivity">GetConnectivity</a>
</td>
<td align="left" width="63%">
Returns the connectivity state of the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetwork-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Returns a description string for the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetwork-getdomaintype">GetDomainType</a>
</td>
<td align="left" width="63%">
Returns the type of network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetwork-getname">GetName</a>
</td>
<td align="left" width="63%">
Returns the name of the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetwork-getnetworkconnections">GetNetworkConnections</a>
</td>
<td align="left" width="63%">
Returns an enumeration of all network connections for a network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetwork-getnetworkid">GetNetworkId</a>
</td>
<td align="left" width="63%">
Returns the unique identifier of a network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetwork-gettimecreatedandconnected">GetTimeCreatedAndConnected</a>
</td>
<td align="left" width="63%">
Returns the local date and time when the network was created and connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetwork-setcategory">SetCategory</a>
</td>
<td align="left" width="63%">
Sets the category of a network. Administrative privileges are needed for this API call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetwork-setdescription">SetDescription</a>
</td>
<td align="left" width="63%">
Sets a new description for the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetwork-setname">SetName</a>
</td>
<td align="left" width="63%">
Sets or renames the network. This change occurs immediately.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetwork</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetwork-get_isconnected">get_IsConnected</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies if the network has any network connectivity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetwork-get_isconnectedtointernet">get_IsConnectedToInternet</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies if the network has internet connectivity.

</td>
</tr>
</table> 


## -remarks



The COM Object that implements <b>INetwork</b> also implements a property bag for additional properties. To get access to this property bag you can use the <b>INetwork</b> interface and <a href="Http://go.microsoft.com/fwlink/p/?linkid=83937">QueryInterface</a> for <a href="Http://go.microsoft.com/fwlink/p/?linkid=83936">IPropertyBag</a>. The property bag on this COM Object contains the following properties:

<table>
<tr>
<th>Parameter</th>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td>NA_DomainAuthenticationFailed</td>
<td>VT_BOOL</td>
<td>Specifies that a domain network is not able to authenticate against the domain controller.</td>
</tr>
<tr>
<td>NA_NetworkClass</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_network_class">NLM_NETWORK_CLASS</a> value stored as VT_UINT </td>
<td>Specifies the class of network. Possible values include:<ul>
<li>
NLM_NETWORK_IDENTIFYING     (0x01)

This is the special "Identifying" network. No properties on this network class can be changed.

</li>
<li>
NLM_NETWORK_IDENTIFIED       (0x02)

This is an Identified network.

</li>
<li>
NLM_NETWORK_UNIDENTIFIED    (0x03)

This is the special "Unidentified" network. The category of this network can be changed, but it will not persist when the network is disconnected.

</li>
</ul>
</td>
</tr>
<tr>
<td>
NA_InternetConnectivityV4 

or

NA_InternetConnectivityV6 

</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_internet_connectivity">NLM_INTERNET_CONNECTIVITY</a> value stored as VT_UINT</td>
<td>
Provides details regarding IPv4 or IPv6 network connectivity. Possible values include:<ul>
<li>
NLM_INTERNET_CONNECTIVITY_WEBHIJACK (0x1)

The detected network is a hotspot. For example, when connected to a coffee Wi-Fi hotspot network and the local HTTP traffic is being redirected to a captive portal, this flag will be set.

</li>
<li>
NLM_INTERNET_CONNECTIVITY_PROXIED (0x2)

The detected network has a proxy configuration. For example, when connected to a corporate network using a proxy for HTTP access, this flag will be set.

</li>
<li>
NLM_INTERNET_CONNECTIVITY_CORPORATE (0x4)

The machine has been configured for Direct Access and access is detected to the corporate domain network Direct Access has been configured for.

</li>
</ul>


</td>
</tr>
<tr>
<td>NA_NameSetByPolicy</td>
<td>VT_BOOL</td>
<td>The name of the network has been set by group policy.</td>
</tr>
<tr>
<td>NA_IconSetByPolicy</td>
<td>VT_BOOL</td>
<td>The icon of the network has been set by group policy.</td>
</tr>
<tr>
<td>NA_DescriptionSetByPolicy</td>
<td>VT_BOOL</td>
<td>The description of the network has been set by group policy.</td>
</tr>
<tr>
<td>NA_CategorySetByPolicy</td>
<td>VT_BOOL</td>
<td>The category of the network has been set by group policy.</td>
</tr>
<tr>
<td>NA_NameReadOnly</td>
<td>VT_BOOL</td>
<td>The name of the network is read only.</td>
</tr>
<tr>
<td>NA_IconReadOnly</td>
<td>VT_BOOL</td>
<td>The icon of the network is read only.</td>
</tr>
<tr>
<td>NA_DescriptionReadOnly</td>
<td>VT_BOOL</td>
<td>The description of the network is read only.</td>
</tr>
<tr>
<td>NA_CategoryReadOnly</td>
<td>VT_BOOL</td>
<td>The category of the network is read only.</td>
</tr>
<tr>
<td>NA_AllowMerge</td>
<td>VT_BOOL</td>
<td>The network can be merged with another network.</td>
</tr>
</table>
 

The <a href="Http://go.microsoft.com/fwlink/p/?linkid=83936">IPropertyBag</a> interface accepts <i>LPCOLESTR</i> as part of the <a href="Http://go.microsoft.com/fwlink/p/?linkid=83934">IPropertyBag::Read</a> and <a href="Http://go.microsoft.com/fwlink/p/?linkid=83936">IPropertyBag::Write</a> methods. For convenience, the string values for these properties are defined inside <b>netlistmgr.h</b> using the same names.



