---
UID: NF:netlistmgr.INetworkListManager.GetNetwork
title: INetworkListManager::GetNetwork (netlistmgr.h)
description: The GetNetwork method retrieves a network based on a supplied network ID.
helpviewer_keywords: ["GetNetwork","GetNetwork method [Network Awareness]","GetNetwork method [Network Awareness]","INetworkListManager interface","INetworkListManager interface [Network Awareness]","GetNetwork method","INetworkListManager.GetNetwork","INetworkListManager::GetNetwork","netlistmgr/INetworkListManager::GetNetwork","nla.inetworklistmanager_getnetwork"]
old-location: nla\inetworklistmanager_getnetwork.htm
tech.root: nla
ms.assetid: a4418884-8df6-4f5b-b9ef-c3cae2bcee47
ms.date: 12/05/2018
ms.keywords: GetNetwork, GetNetwork method [Network Awareness], GetNetwork method [Network Awareness],INetworkListManager interface, INetworkListManager interface [Network Awareness],GetNetwork method, INetworkListManager.GetNetwork, INetworkListManager::GetNetwork, netlistmgr/INetworkListManager::GetNetwork, nla.inetworklistmanager_getnetwork
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
 - INetworkListManager::GetNetwork
 - netlistmgr/INetworkListManager::GetNetwork
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
 - INetworkListManager.GetNetwork
---

# INetworkListManager::GetNetwork


## -description

The <b>GetNetwork</b> method retrieves a network based on a supplied network ID.

## -parameters

### -param gdNetworkId [in]

GUID that specifies the network ID.

### -param ppNetwork [out]

Pointer to a pointer that receives the <a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetwork">INetwork</a> interface instance for this network.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The GUID is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworklistmanager">INetworkListManager</a>