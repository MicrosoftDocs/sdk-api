---
UID: NN:netlistmgr.INetwork
title: INetwork (netlistmgr.h)
description: The INetwork interface represents a network on the local machine. It can also represent a collection of network connections with a similar network signature.
helpviewer_keywords: ["INetwork","INetwork interface [Network Awareness]","INetwork interface [Network Awareness]","described","netlistmgr/INetwork","nla.inetwork"]
old-location: nla\inetwork.htm
tech.root: nla
ms.assetid: 6d483058-f7c4-4a6c-a1a8-816c2fab9994
ms.date: 12/05/2018
ms.keywords: INetwork, INetwork interface [Network Awareness], INetwork interface [Network Awareness],described, netlistmgr/INetwork, nla.inetwork
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetwork
 - netlistmgr/INetwork
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetwork
---

# INetwork interface


## -description

The <b>INetwork</b> interface represents a network on the local machine. It can also represent a collection of network connections with a similar network signature.

## -inheritance

The <b>INetwork</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INetwork</b> also has these types of members:

## -remarks

The COM Object that implements <b>INetwork</b> also implements a property bag for additional properties. To get access to this property bag you can use the <b>INetwork</b> interface and <a href="/previous-versions/windows/embedded/ms890661(v=msdn.10)">QueryInterface</a> for <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a>. The property bag on this COM Object contains the following properties:

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
<a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_network_class">NLM_NETWORK_CLASS</a> value stored as VT_UINT </td>
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
<a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_internet_connectivity">NLM_INTERNET_CONNECTIVITY</a> value stored as VT_UINT</td>
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
 

The <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> interface accepts <i>LPCOLESTR</i> as part of the <a href="/previous-versions/windows/embedded/ms884257(v=msdn.10)">IPropertyBag::Read</a> and <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag::Write</a> methods. For convenience, the string values for these properties are defined inside <b>netlistmgr.h</b> using the same names.
