---
UID: NN:netlistmgr.IEnumNetworks
title: IEnumNetworks (netlistmgr.h)
description: The IEnumNetworks interface is a standard enumerator for networks. It enumerates all networks available on the local machine. This interface can be obtained from the INetworkListManager interface.
helpviewer_keywords: ["IEnumNetworks","IEnumNetworks interface [Network Awareness]","IEnumNetworks interface [Network Awareness]","described","netlistmgr/IEnumNetworks","nla.ienumnetworks"]
old-location: nla\ienumnetworks.htm
tech.root: nla
ms.assetid: ce2b65e5-89fe-48c9-aa00-373406891d02
ms.date: 12/05/2018
ms.keywords: IEnumNetworks, IEnumNetworks interface [Network Awareness], IEnumNetworks interface [Network Awareness],described, netlistmgr/IEnumNetworks, nla.ienumnetworks
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
 - IEnumNetworks
 - netlistmgr/IEnumNetworks
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
 - IEnumNetworks
---

# IEnumNetworks interface


## -description

The <b>IEnumNetworks</b> interface is a standard enumerator for networks. It enumerates all networks available on the local machine. This interface can be obtained from the <a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworklistmanager">INetworkListManager</a> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumNetworks</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumNetworks</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IEnumNetworks</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-ienumnetworks-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates an enumerator that contains the same enumeration state as the enumerator currently in use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-ienumnetworks-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-ienumnetworks-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-ienumnetworks-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumNetworks</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-ienumnetworks-get__newenum">get__NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns an automation enumerator object that you can use to iterate through the <b>IEnumNetworks</b> collection.

</td>
</tr>
</table>

## -remarks

The list of connected or disconnected networks is cached by <b>IEnumNetworks</b> when it is instantiated. This list is not updated when the connectivity state of a network changes. The <a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetwork">INetwork</a> interface is recommended for retrieving the current  connectivity state of a network.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworklistmanager">INetworkListManager</a>