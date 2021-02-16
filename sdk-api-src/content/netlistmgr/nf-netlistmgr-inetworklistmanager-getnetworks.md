---
UID: NF:netlistmgr.INetworkListManager.GetNetworks
title: INetworkListManager::GetNetworks (netlistmgr.h)
description: The GetNetworks method retrieves the list of networks available on the local machine.
helpviewer_keywords: ["GetNetworks","GetNetworks method [Network Awareness]","GetNetworks method [Network Awareness]","INetworkListManager interface","INetworkListManager interface [Network Awareness]","GetNetworks method","INetworkListManager.GetNetworks","INetworkListManager::GetNetworks","netlistmgr/INetworkListManager::GetNetworks","nla.inetworklistmanager_getnetworks"]
old-location: nla\inetworklistmanager_getnetworks.htm
tech.root: nla
ms.assetid: 547ab687-b323-4fd7-8c08-80a79352a626
ms.date: 12/05/2018
ms.keywords: GetNetworks, GetNetworks method [Network Awareness], GetNetworks method [Network Awareness],INetworkListManager interface, INetworkListManager interface [Network Awareness],GetNetworks method, INetworkListManager.GetNetworks, INetworkListManager::GetNetworks, netlistmgr/INetworkListManager::GetNetworks, nla.inetworklistmanager_getnetworks
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
 - INetworkListManager::GetNetworks
 - netlistmgr/INetworkListManager::GetNetworks
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
 - INetworkListManager.GetNetworks
---

# INetworkListManager::GetNetworks


## -description

The <b>GetNetworks</b> method retrieves the list of networks available on the local machine.

## -parameters

### -param Flags [in]

<a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_enum_network">NLM_ENUM_NETWORK</a> enumeration value that specifies the flags for the network (specifically, connected or not connected).

### -param ppEnumNetwork [out]

Pointer to a pointer that receives an <a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-ienumnetworks">IEnumNetworks</a> interface instance that contains the enumerator for the list of available networks.

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