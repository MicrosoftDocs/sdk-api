---
UID: NF:netlistmgr.INetworkListManager.GetNetworkConnections
title: INetworkListManager::GetNetworkConnections
author: windows-driver-content
description: The GetNetworkConnections method enumerates a complete list of the network connections that have been made.
old-location: nla\inetworklistmanager_getnetworkconnections.htm
old-project: NLA
ms.assetid: ddbf02ae-3232-4866-b4c1-e4611b680f9f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetNetworkConnections, GetNetworkConnections method [Network Awareness], GetNetworkConnections method [Network Awareness],INetworkListManager interface, INetworkListManager interface [Network Awareness],GetNetworkConnections method, INetworkListManager.GetNetworkConnections, INetworkListManager::GetNetworkConnections, netlistmgr/INetworkListManager::GetNetworkConnections, nla.inetworklistmanager_getnetworkconnections
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: NLM_NETWORK_PROPERTY_CHANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Netlistmgr.h
api_name:
-	INetworkListManager.GetNetworkConnections
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetworkListManager::GetNetworkConnections


## -description


The <b>GetNetworkConnections</b> method enumerates a complete list of the network connections that have been made.


## -parameters




### -param ppEnum [out]

Pointer to a pointer that receives an <a href="https://msdn.microsoft.com/f7e69ede-c567-4285-a017-096c94fb3fe4">IEnumNetworkConnections</a> interface instance that enumerates all network connections on the machine.


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




<a href="https://msdn.microsoft.com/a9f76b6a-ea15-47b7-a4ef-14ea60b7810d">INetworkListManager</a>
 

 

