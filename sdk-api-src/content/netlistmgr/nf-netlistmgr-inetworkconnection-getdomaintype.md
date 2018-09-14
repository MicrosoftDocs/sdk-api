---
UID: NF:netlistmgr.INetworkConnection.GetDomainType
title: INetworkConnection::GetDomainType
author: windows-sdk-content
description: The GetDomainType method returns the domain type of the network connection.
old-location: nla\inetworkconnection_getdomaintype.htm
tech.root: NLA
ms.assetid: e243c1a3-8166-4e08-80f5-32811bcada69
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetDomainType, GetDomainType method [Network Awareness], GetDomainType method [Network Awareness],INetworkConnection interface, INetworkConnection interface [Network Awareness],GetDomainType method, INetworkConnection.GetDomainType, INetworkConnection::GetDomainType, netlistmgr/INetworkConnection::GetDomainType, nla.inetworkconnection_getdomaintype
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
 - INetworkConnection.GetDomainType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetworkConnection::GetDomainType


## -description


The <b>GetDomainType</b> method returns the domain type of the network connection.


## -parameters




### -param pDomainType [out]

Pointer to an <a href="https://msdn.microsoft.com/fd1bc50a-c8d3-4594-870e-3bbb5c6ea1da">NLM_DOMAIN_TYPE</a> enumeration value that specifies the domain type of the network.


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/666761b5-0146-438d-9986-ecce3b45b5ff">INetworkConnection</a>
 

 

