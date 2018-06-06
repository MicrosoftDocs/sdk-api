---
UID: NF:netlistmgr.INetwork.GetConnectivity
title: INetwork::GetConnectivity
author: windows-sdk-content
description: The GetConnectivity method returns the connectivity state of the network.
old-location: nla\inetwork_getconnectivity.htm
old-project: NLA
ms.assetid: 04191757-7d9f-4211-a311-4863d62bd0a5
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetConnectivity, GetConnectivity method [Network Awareness], GetConnectivity method [Network Awareness],INetwork interface, INetwork interface [Network Awareness],GetConnectivity method, INetwork.GetConnectivity, INetwork::GetConnectivity, netlistmgr/INetwork::GetConnectivity, nla.inetwork_getconnectivity
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
 - INetwork.GetConnectivity
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetwork::GetConnectivity


## -description


The <b>GetConnectivity</b> method returns the connectivity state of the network.


## -parameters




### -param pConnectivity [out]

Pointer to a <a href="https://msdn.microsoft.com/72d1f049-3c8d-4332-9bf1-9f49b47cd315">NLM_CONNECTIVITY</a> enumeration value that contains a bitmask  that specifies the connectivity state of this network.


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/6d483058-f7c4-4a6c-a1a8-816c2fab9994">INetwork</a>



<a href="https://msdn.microsoft.com/72d1f049-3c8d-4332-9bf1-9f49b47cd315">NLM_CONNECTIVITY</a>
 

 

