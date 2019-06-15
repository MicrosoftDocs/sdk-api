---
UID: NN:netlistmgr.INetworkListManagerEvents
title: INetworkListManagerEvents (netlistmgr.h)
author: windows-sdk-content
description: INetworkListManagerEvents is a message sink interface that a client implements to get overall machine state related events. Applications that are interested on higher-level events, for example internet connectivity, implement this interface.
old-location: nla\inetworklistmanagerevents.htm
tech.root: nla
ms.assetid: cdcb661f-5f17-481a-a4b7-db06d53e1b97
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INetworkListManagerEvents, INetworkListManagerEvents interface [Network Awareness], INetworkListManagerEvents interface [Network Awareness],described, netlistmgr/INetworkListManagerEvents, nla.inetworklistmanagerevents
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
 - INetworkListManagerEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetworkListManagerEvents interface


## -description


<b>INetworkListManagerEvents</b> is a message sink interface that a client implements to get overall machine state related events. Applications that are interested on higher-level events, for example internet connectivity, implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetworkListManagerEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INetworkListManagerEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetworkListManagerEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworklistmanagerevents-connectivitychanged">ConnectivityChanged</a>
</td>
<td align="left" width="63%">
Called when network connectivity related changes occur. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connectivity">NLM_CONNECTIVITY</a>
 

 

