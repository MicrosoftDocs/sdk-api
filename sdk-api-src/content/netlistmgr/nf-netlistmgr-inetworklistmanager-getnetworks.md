---
UID: NF:netlistmgr.INetworkListManager.GetNetworks
title: INetworkListManager::GetNetworks
author: windows-driver-content
description: The GetNetworks method retrieves the list of networks available on the local machine.
old-location: nla\inetworklistmanager_getnetworks.htm
old-project: NLA
ms.assetid: 547ab687-b323-4fd7-8c08-80a79352a626
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetNetworks, GetNetworks method [Network Awareness], GetNetworks method [Network Awareness],INetworkListManager interface, INetworkListManager interface [Network Awareness],GetNetworks method, INetworkListManager.GetNetworks, INetworkListManager::GetNetworks, netlistmgr/INetworkListManager::GetNetworks, nla.inetworklistmanager_getnetworks
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
-	INetworkListManager.GetNetworks
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetworkListManager::GetNetworks


## -description


The <b>GetNetworks</b> method retrieves the list of networks available on the local machine.


## -parameters




### -param Flags [in]


<a href="https://msdn.microsoft.com/37eb1e2e-d769-4e58-b93d-582312bd500a">NLM_ENUM_NETWORK</a> enumeration value that specifies the flags for the network (specifically, connected or not connected).


### -param ppEnumNetwork [out]

Pointer to a pointer that receives an <a href="https://msdn.microsoft.com/ce2b65e5-89fe-48c9-aa00-373406891d02">IEnumNetworks</a> interface instance that contains the enumerator for the list of available networks.


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
 

 

