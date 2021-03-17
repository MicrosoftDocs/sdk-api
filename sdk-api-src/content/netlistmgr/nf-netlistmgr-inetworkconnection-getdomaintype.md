---
UID: NF:netlistmgr.INetworkConnection.GetDomainType
title: INetworkConnection::GetDomainType (netlistmgr.h)
description: The GetDomainType method returns the domain type of the network connection.
helpviewer_keywords: ["GetDomainType","GetDomainType method [Network Awareness]","GetDomainType method [Network Awareness]","INetworkConnection interface","INetworkConnection interface [Network Awareness]","GetDomainType method","INetworkConnection.GetDomainType","INetworkConnection::GetDomainType","netlistmgr/INetworkConnection::GetDomainType","nla.inetworkconnection_getdomaintype"]
old-location: nla\inetworkconnection_getdomaintype.htm
tech.root: nla
ms.assetid: e243c1a3-8166-4e08-80f5-32811bcada69
ms.date: 12/05/2018
ms.keywords: GetDomainType, GetDomainType method [Network Awareness], GetDomainType method [Network Awareness],INetworkConnection interface, INetworkConnection interface [Network Awareness],GetDomainType method, INetworkConnection.GetDomainType, INetworkConnection::GetDomainType, netlistmgr/INetworkConnection::GetDomainType, nla.inetworkconnection_getdomaintype
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
 - INetworkConnection::GetDomainType
 - netlistmgr/INetworkConnection::GetDomainType
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
 - INetworkConnection.GetDomainType
---

# INetworkConnection::GetDomainType


## -description

The <b>GetDomainType</b> method returns the domain type of the network connection.

## -parameters

### -param pDomainType [out]

Pointer to an <a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_domain_type">NLM_DOMAIN_TYPE</a> enumeration value that specifies the domain type of the network.

## -returns

Returns S_OK if the method succeeds.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkconnection">INetworkConnection</a>