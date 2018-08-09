---
UID: NF:netlistmgr.INetworkListManager.get_IsConnectedToInternet
title: INetworkListManager::get_IsConnectedToInternet
author: windows-sdk-content
description: The get_IsConnectedToInternet property specifies if the local machine has internet connectivity.
old-location: nla\inetworklistmanager_get_isconnectedtointernet.htm
old-project: nla
ms.assetid: b3f06da5-c0e2-4c56-87af-b180aa87c827
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: INetworkListManager interface [Network Awareness],get_IsConnectedToInternet method, INetworkListManager.get_IsConnectedToInternet, INetworkListManager::get_IsConnectedToInternet, get_IsConnectedToInternet, get_IsConnectedToInternet method [Network Awareness], get_IsConnectedToInternet method [Network Awareness],INetworkListManager interface, netlistmgr/INetworkListManager::get_IsConnectedToInternet, nla.inetworklistmanager_get_isconnectedtointernet
ms.prod: windows
ms.technology: windows-sdk
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
 - INetworkListManager.get_IsConnectedToInternet
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetworkListManager::get_IsConnectedToInternet


## -description


The <b>get_IsConnectedToInternet</b> property specifies if the local machine has internet connectivity.


## -parameters




### -param pbIsConnected [out]

If <b>TRUE</b>, the local machine is connected to the internet; if <b>FALSE</b>, it is not.


## -returns



Returns S_OK if successful.




## -see-also




<a href="https://msdn.microsoft.com/a9f76b6a-ea15-47b7-a4ef-14ea60b7810d">INetworkListManager</a>
 

 

