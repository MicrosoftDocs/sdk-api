---
UID: NF:netlistmgr.INetworkListManager.GetNetworkConnections
title: INetworkListManager::GetNetworkConnections (netlistmgr.h)
description: The GetNetworkConnections method enumerates a complete list of the network connections that have been made.
helpviewer_keywords: ["GetNetworkConnections","GetNetworkConnections method [Network Awareness]","GetNetworkConnections method [Network Awareness]","INetworkListManager interface","INetworkListManager interface [Network Awareness]","GetNetworkConnections method","INetworkListManager.GetNetworkConnections","INetworkListManager::GetNetworkConnections","netlistmgr/INetworkListManager::GetNetworkConnections","nla.inetworklistmanager_getnetworkconnections"]
old-location: nla\inetworklistmanager_getnetworkconnections.htm
tech.root: nla
ms.assetid: ddbf02ae-3232-4866-b4c1-e4611b680f9f
ms.date: 12/05/2018
ms.keywords: GetNetworkConnections, GetNetworkConnections method [Network Awareness], GetNetworkConnections method [Network Awareness],INetworkListManager interface, INetworkListManager interface [Network Awareness],GetNetworkConnections method, INetworkListManager.GetNetworkConnections, INetworkListManager::GetNetworkConnections, netlistmgr/INetworkListManager::GetNetworkConnections, nla.inetworklistmanager_getnetworkconnections
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
 - INetworkListManager::GetNetworkConnections
 - netlistmgr/INetworkListManager::GetNetworkConnections
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
 - INetworkListManager.GetNetworkConnections
---

# INetworkListManager::GetNetworkConnections


## -description

The <b>GetNetworkConnections</b> method enumerates a complete list of the network connections that have been made.

## -parameters

### -param ppEnum [out]

Pointer to a pointer that receives an <a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-ienumnetworkconnections">IEnumNetworkConnections</a> interface instance that enumerates all network connections on the machine.

## -returns

Returns S_OK if the method succeeds. Otherwise, the method returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The pointer passed is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworklistmanager">INetworkListManager</a>