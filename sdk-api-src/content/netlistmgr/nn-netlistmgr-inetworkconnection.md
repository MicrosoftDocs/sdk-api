---
UID: NN:netlistmgr.INetworkConnection
title: INetworkConnection (netlistmgr.h)
description: The INetworkConnection interface represents a single network connection.
helpviewer_keywords: ["INetworkConnection","INetworkConnection interface [Network Awareness]","INetworkConnection interface [Network Awareness]","described","netlistmgr/INetworkConnection","nla.inetworkconnection"]
old-location: nla\inetworkconnection.htm
tech.root: nla
ms.assetid: 666761b5-0146-438d-9986-ecce3b45b5ff
ms.date: 12/05/2018
ms.keywords: INetworkConnection, INetworkConnection interface [Network Awareness], INetworkConnection interface [Network Awareness],described, netlistmgr/INetworkConnection, nla.inetworkconnection
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
 - INetworkConnection
 - netlistmgr/INetworkConnection
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
 - INetworkConnection
---

# INetworkConnection interface


## -description

The <b>INetworkConnection</b> interface represents a single network connection.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetworkConnection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INetworkConnection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetworkConnection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkconnection-getadapterid">GetAdapterId</a>
</td>
<td align="left" width="63%">
Returns the ID of the network adapter used by this connection. There may multiple connections using the same adapter ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkconnection-getconnectionid">GetConnectionId</a>
</td>
<td align="left" width="63%">
Returns the Connection ID associated with this network connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkconnection-getconnectivity">GetConnectivity</a>
</td>
<td align="left" width="63%">
Returns the connectivity state of the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkconnection-getdomaintype">GetDomainType</a>
</td>
<td align="left" width="63%">
Returns the type of network connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkconnection-getnetwork">GetNetwork</a>
</td>
<td align="left" width="63%">
Returns the associated network for the connection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetworkConnection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkconnection-get_isconnected">get_IsConnected</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies if the associated network has any network connectivity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkconnection-get_isconnectedtointernet">get_IsConnectedToInternet</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies if the associated network has any internet connectivity.

</td>
</tr>
</table>