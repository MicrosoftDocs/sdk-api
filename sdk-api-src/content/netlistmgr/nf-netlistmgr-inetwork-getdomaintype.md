---
UID: NF:netlistmgr.INetwork.GetDomainType
title: INetwork::GetDomainType
author: windows-sdk-content
description: The GetDomainType method returns the domain type of a network.
old-location: nla\inetwork_getdomaintype.htm
old-project: NLA
ms.assetid: ca23d7c0-fe25-4375-bd2c-6c2ccae56548
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetDomainType, GetDomainType method [Network Awareness], GetDomainType method [Network Awareness],INetwork interface, INetwork interface [Network Awareness],GetDomainType method, INetwork.GetDomainType, INetwork::GetDomainType, netlistmgr/INetwork::GetDomainType, nla.inetwork_getdomaintype
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Netlistmgr.h
api_name:
-	INetwork.GetDomainType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetwork::GetDomainType


## -description


The GetDomainType method returns the domain type of a network.


## -parameters




### -param pNetworkType [out]

Pointer to an <a href="https://msdn.microsoft.com/fd1bc50a-c8d3-4594-870e-3bbb5c6ea1da">NLM_DOMAIN_TYPE</a> enumeration value that specifies the domain type of the network.


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/6d483058-f7c4-4a6c-a1a8-816c2fab9994">INetwork</a>
 

 

