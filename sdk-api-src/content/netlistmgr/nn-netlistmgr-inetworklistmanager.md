---
UID: NN:netlistmgr.INetworkListManager
title: INetworkListManager (netlistmgr.h)
description: The INetworkListManager interface provides a set of methods to perform network list management functions.
helpviewer_keywords: ["INetworkListManager","INetworkListManager interface [Network Awareness]","INetworkListManager interface [Network Awareness]","described","netlistmgr/INetworkListManager","nla.inetworklistmanager"]
old-location: nla\inetworklistmanager.htm
tech.root: nla
ms.assetid: a9f76b6a-ea15-47b7-a4ef-14ea60b7810d
ms.date: 12/05/2018
ms.keywords: INetworkListManager, INetworkListManager interface [Network Awareness], INetworkListManager interface [Network Awareness],described, netlistmgr/INetworkListManager, nla.inetworklistmanager
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
 - INetworkListManager
 - netlistmgr/INetworkListManager
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
 - INetworkListManager
---

# INetworkListManager interface


## -description

The <b>INetworkListManager</b> interface provides a set of methods to perform network list management functions.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetworkListManager</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetworkListManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetworkListManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworklistmanager-clearsimulatedprofileinfo">ClearSimulatedProfileInfo</a>
</td>
<td align="left" width="63%">
Clears the connection profile values previously applied to the internet profile by <a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworklistmanager-setsimulatedprofileinfo">SetSimulatedProfileInfo</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworklistmanager-getconnectivity">GetConnectivity</a>
</td>
<td align="left" width="63%">
Returns the connectivity state of all the networks on a machine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworklistmanager-getnetwork">GetNetwork</a>
</td>
<td align="left" width="63%">
Retrieves a network based on a supplied Network ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworklistmanager-getnetworkconnections">GetNetworkConnections</a>
</td>
<td align="left" width="63%">
Gets an enumerator that contains a complete list of the network connections that have been made.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworklistmanager-getnetworks">GetNetworks</a>
</td>
<td align="left" width="63%">
Retrieves networks based on the supplied Network IDs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworklistmanager-setsimulatedprofileinfo">SetSimulatedProfileInfo</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworklistmanager-setsimulatedprofileinfo">SetSimulatedProfileInfo</a> method applies a specific set of connection profile values to an internet profile in support of the simulation of specific metered internet connection conditions using the Visual Studio Simulator.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetworkListManager</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworklistmanager-get_isconnected">get_IsConnected</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies if the machine has network connectivity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworklistmanager-get_isconnectedtointernet">get_IsConnectedToInternet</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies if the machine has Internet connectivity.

</td>
</tr>
</table>