---
UID: NN:netlistmgr.IEnumNetworkConnections
title: IEnumNetworkConnections (netlistmgr.h)

description: The IEnumNetworkConnections interface provides a standard enumerator for network connections. It enumerates active, disconnected, or all network connections within a network. This interface can be obtained from the INetwork interface.
old-location: nla\ienumnetworkconnections.htm
tech.root: nla
ms.assetid: f7e69ede-c567-4285-a017-096c94fb3fe4

ms.date: 12/05/2018
ms.keywords: IEnumNetworkConnections, IEnumNetworkConnections interface [Network Awareness], IEnumNetworkConnections interface [Network Awareness],described, netlistmgr/IEnumNetworkConnections, nla.ienumnetworkconnections
ms.topic: interface
f1_keywords: 
 - "netlistmgr/IEnumNetworkConnections"
dev_langs:
 - c++
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
 - IEnumNetworkConnections
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumNetworkConnections interface


## -description


The IEnumNetworkConnections interface provides  a standard enumerator for network connections. It enumerates active, disconnected, or all network connections within a network. This interface can be obtained from the <a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nn-netlistmgr-inetwork">INetwork</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumNetworkConnections</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumNetworkConnections</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IEnumNetworkConnections</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-ienumnetworkconnections-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates an enumerator that contains the same enumeration state as the enumerator currently in use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-ienumnetworkconnections-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-ienumnetworkconnections-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-ienumnetworkconnections-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumNetworkConnections</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-ienumnetworkconnections-get__newenum">get__NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns an automation enumerator object that you can use to iterate through the IEnumNetworkConnections collection from Visual Basic and .NET languages through COM interop.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nn-netlistmgr-inetwork">INetwork</a>
 

 

