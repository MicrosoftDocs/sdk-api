---
UID: NF:netlistmgr.INetworkListManager.GetNetworkConnection
title: INetworkListManager::GetNetworkConnection (netlistmgr.h)
description: The GetNetworkConnection method retrieves a network based on a supplied Network Connection ID.
helpviewer_keywords: ["GetNetworkConnection","GetNetworkConnection method [Network Awareness]","GetNetworkConnection method [Network Awareness]","INetworkListManager interface","INetworkListManager interface [Network Awareness]","GetNetworkConnection method","INetworkListManager.GetNetworkConnection","INetworkListManager::GetNetworkConnection","netlistmgr/INetworkListManager::GetNetworkConnection","nla.inetworklistmanager_getnetworkconnection"]
old-location: nla\inetworklistmanager_getnetworkconnection.htm
tech.root: nla
ms.assetid: d57341f1-5f73-4d6d-964f-cb80cfbedf1b
ms.date: 12/05/2018
ms.keywords: GetNetworkConnection, GetNetworkConnection method [Network Awareness], GetNetworkConnection method [Network Awareness],INetworkListManager interface, INetworkListManager interface [Network Awareness],GetNetworkConnection method, INetworkListManager.GetNetworkConnection, INetworkListManager::GetNetworkConnection, netlistmgr/INetworkListManager::GetNetworkConnection, nla.inetworklistmanager_getnetworkconnection
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
 - INetworkListManager::GetNetworkConnection
 - netlistmgr/INetworkListManager::GetNetworkConnection
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
 - INetworkListManager.GetNetworkConnection
---

# INetworkListManager::GetNetworkConnection


## -description

The <b>GetNetworkConnection</b> method retrieves a network based on a supplied Network Connection ID.

## -parameters

### -param gdNetworkConnectionId [in]

A <b>GUID</b> that specifies the Network Connection ID.

### -param ppNetworkConnection [out, retval]

Pointer to a pointer to the <a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkconnection">INetworkConnection</a> object associated with the supplied <i>gdNetworkConnectionId</i>.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The network associated with the specified network connection ID was not found.

</td>
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
The specified GUID is invalid.

</td>
</tr>
</table>

## -remarks

This method can return <b>S_FALSE</b> if a network connection associated with the specified ID has been removed. 
For example, it is possible for  a client to receive a <a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkconnectionevents-networkconnectionconnectivitychanged">INetworkConnectionEvents::NetworkConnectionConnectivityChanged</a> event along with a network connection ID, but find that the network connection has been disconnected or even replaced by the time  <b>INetworkListManager::GetNetworkConnection</b> is called with the provided ID.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkconnection">INetworkConnection</a>



<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworklistmanager">INetworkListManager</a>