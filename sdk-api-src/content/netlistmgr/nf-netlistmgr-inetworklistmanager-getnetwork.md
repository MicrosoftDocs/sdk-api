---
UID: NF:netlistmgr.INetworkListManager.GetNetwork
title: INetworkListManager::GetNetwork
author: windows-sdk-content
description: The GetNetwork method retrieves a network based on a supplied network ID.
old-location: nla\inetworklistmanager_getnetwork.htm
old-project: nla
ms.assetid: a4418884-8df6-4f5b-b9ef-c3cae2bcee47
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetNetwork, GetNetwork method [Network Awareness], GetNetwork method [Network Awareness],INetworkListManager interface, INetworkListManager interface [Network Awareness],GetNetwork method, INetworkListManager.GetNetwork, INetworkListManager::GetNetwork, netlistmgr/INetworkListManager::GetNetwork, nla.inetworklistmanager_getnetwork
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: netlistmgr.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: NLM_NETWORK_PROPERTY_CHANGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetworkListManager.GetNetwork
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetworkListManager::GetNetwork


## -description


The <b>GetNetwork</b> method retrieves a network based on a supplied network ID.


## -parameters




### -param gdNetworkId [in]

GUID that specifies the network ID.


### -param ppNetwork [out]

Pointer to a pointer that receives the <a href="https://msdn.microsoft.com/6d483058-f7c4-4a6c-a1a8-816c2fab9994">INetwork</a> interface instance for this network.


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




<a href="https://msdn.microsoft.com/a9f76b6a-ea15-47b7-a4ef-14ea60b7810d">INetworkListManager</a>
 

 

