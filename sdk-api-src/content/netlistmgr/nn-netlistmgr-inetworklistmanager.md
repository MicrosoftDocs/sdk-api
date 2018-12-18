---
UID: NN:netlistmgr.INetworkListManager
title: INetworkListManager
author: windows-sdk-content
description: The INetworkListManager interface provides a set of methods to perform network list management functions.
old-location: nla\inetworklistmanager.htm
tech.root: nla
ms.assetid: a9f76b6a-ea15-47b7-a4ef-14ea60b7810d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INetworkListManager, INetworkListManager interface [Network Awareness], INetworkListManager interface [Network Awareness],described, netlistmgr/INetworkListManager, nla.inetworklistmanager
ms.topic: interface
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
 - INetworkListManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetworkListManager interface


## -description


The <b>INetworkListManager</b> interface provides a set of methods to perform network list management functions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetworkListManager</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>INetworkListManager</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/DD89717F-4BFD-4283-A9F4-A74BB6E8E8D6">ClearSimulatedProfileInfo</a>
</td>
<td align="left" width="63%">
Clears the connection profile values previously applied to the internet profile by <a href="https://msdn.microsoft.com/168501A6-F8B2-4635-97BB-538994074D2C">SetSimulatedProfileInfo</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4695554a-2f8b-4d2e-b3ff-ec22c43387d6">GetConnectivity</a>
</td>
<td align="left" width="63%">
Returns the connectivity state of all the networks on a machine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4418884-8df6-4f5b-b9ef-c3cae2bcee47">GetNetwork</a>
</td>
<td align="left" width="63%">
Retrieves a network based on a supplied Network ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddbf02ae-3232-4866-b4c1-e4611b680f9f">GetNetworkConnections</a>
</td>
<td align="left" width="63%">
Gets an enumerator that contains a complete list of the network connections that have been made.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/547ab687-b323-4fd7-8c08-80a79352a626">GetNetworks</a>
</td>
<td align="left" width="63%">
Retrieves networks based on the supplied Network IDs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/168501A6-F8B2-4635-97BB-538994074D2C">SetSimulatedProfileInfo</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/168501A6-F8B2-4635-97BB-538994074D2C">SetSimulatedProfileInfo</a> method applies a specific set of connection profile values to an internet profile in support of the simulation of specific metered internet connection conditions using the Visual Studio Simulator.

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

<a href="https://msdn.microsoft.com/51bdec8e-521f-4673-a2ad-07e8995f3905">get_IsConnected</a>


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

<a href="https://msdn.microsoft.com/b3f06da5-c0e2-4c56-87af-b180aa87c827">get_IsConnectedToInternet</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies if the machine has Internet connectivity.

</td>
</tr>
</table> 

