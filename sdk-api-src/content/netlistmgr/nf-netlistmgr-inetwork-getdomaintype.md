---
UID: NF:netlistmgr.INetwork.GetDomainType
title: INetwork::GetDomainType (netlistmgr.h)
author: windows-sdk-content
description: The GetDomainType method returns the domain type of a network.
old-location: nla\inetwork_getdomaintype.htm
tech.root: nla
ms.assetid: ca23d7c0-fe25-4375-bd2c-6c2ccae56548
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDomainType, GetDomainType method [Network Awareness], GetDomainType method [Network Awareness],INetwork interface, INetwork interface [Network Awareness],GetDomainType method, INetwork.GetDomainType, INetwork::GetDomainType, netlistmgr/INetwork::GetDomainType, nla.inetwork_getdomaintype
ms.topic: method
f1_keywords: 
 - "netlistmgr/INetwork.GetDomainType"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetwork.GetDomainType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetwork::GetDomainType


## -description


The GetDomainType method returns the domain type of a network.


## -parameters




### -param pNetworkType [out]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_domain_type">NLM_DOMAIN_TYPE</a> enumeration value that specifies the domain type of the network.


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nn-netlistmgr-inetwork">INetwork</a>
 

 

