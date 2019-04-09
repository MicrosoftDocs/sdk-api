---
UID: NN:netlistmgr.IEnumNetworks
title: IEnumNetworks (netlistmgr.h)
author: windows-sdk-content
description: The IEnumNetworks interface is a standard enumerator for networks. It enumerates all networks available on the local machine. This interface can be obtained from the INetworkListManager interface.
old-location: nla\ienumnetworks.htm
tech.root: nla
ms.assetid: ce2b65e5-89fe-48c9-aa00-373406891d02
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumNetworks, IEnumNetworks interface [Network Awareness], IEnumNetworks interface [Network Awareness],described, netlistmgr/IEnumNetworks, nla.ienumnetworks
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
 - IEnumNetworks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumNetworks interface


## -description


The <b>IEnumNetworks</b> interface is a standard enumerator for networks. It enumerates all networks available on the local machine. This interface can be obtained from the <a href="https://msdn.microsoft.com/a9f76b6a-ea15-47b7-a4ef-14ea60b7810d">INetworkListManager</a> interface. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumNetworks</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumNetworks</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/196bf9fa-4615-44c3-accf-f70516d5a6a5">Clone</a>
</td>
<td align="left" width="63%">
Creates an enumerator that contains the same enumeration state as the enumerator currently in use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ee2501c-502e-448e-8635-c8bf9d169ebb">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f866f7e1-385c-476e-baf6-b028592fcd0b">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f39e65e-6ff4-4fc5-a7fe-5f83a0b3f5e7">Skip</a>
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

<a href="https://msdn.microsoft.com/ddff98c2-669d-4f8d-9584-b8590705c2f0">get__NewEnum</a>


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



The list of connected or disconnected networks is cached by <b>IEnumNetworks</b> when it is instantiated. This list is not updated when the connectivity state of a network changes. The <a href="https://msdn.microsoft.com/6d483058-f7c4-4a6c-a1a8-816c2fab9994">INetwork</a> interface is recommended for retrieving the current  connectivity state of a network.




## -see-also




<a href="https://msdn.microsoft.com/a9f76b6a-ea15-47b7-a4ef-14ea60b7810d">INetworkListManager</a>
 

 

