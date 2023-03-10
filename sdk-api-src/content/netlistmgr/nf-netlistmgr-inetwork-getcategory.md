---
UID: NF:netlistmgr.INetwork.GetCategory
title: INetwork::GetCategory (netlistmgr.h)
description: The GetCategory method returns the category of a network.
helpviewer_keywords: ["GetCategory","GetCategory method [Network Awareness]","GetCategory method [Network Awareness]","INetwork interface","INetwork interface [Network Awareness]","GetCategory method","INetwork.GetCategory","INetwork::GetCategory","netlistmgr/INetwork::GetCategory","nla.inetwork_getcategory"]
old-location: nla\inetwork_getcategory.htm
tech.root: nla
ms.assetid: 8a57c6ad-8c6c-4ef0-a731-463a5d7e325f
ms.date: 12/05/2018
ms.keywords: GetCategory, GetCategory method [Network Awareness], GetCategory method [Network Awareness],INetwork interface, INetwork interface [Network Awareness],GetCategory method, INetwork.GetCategory, INetwork::GetCategory, netlistmgr/INetwork::GetCategory, nla.inetwork_getcategory
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
 - INetwork::GetCategory
 - netlistmgr/INetwork::GetCategory
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
 - INetwork.GetCategory
---

# INetwork::GetCategory


## -description

The <b>GetCategory</b> method returns the category of a network.

## -parameters

### -param pCategory [out]

Pointer to a <a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_network_category">NLM_NETWORK_CATEGORY</a> enumeration value that specifies the category information for the network.

## -returns

Returns S_OK if the method succeeds.

## -remarks

The private or public network categories must never be used to assume  which Windows Firewall ports are open, as the user can change the default settings of these categories. Instead, Windows Firewall APIs should be called to ensure the ports that the required ports are open.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetwork">INetwork</a>



<a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_network_category">NLM_NETWORK_CATEGORY</a>