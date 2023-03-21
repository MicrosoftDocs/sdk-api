---
UID: NE:netlistmgr.NLM_NETWORK_CATEGORY
title: NLM_NETWORK_CATEGORY (netlistmgr.h)
description: The NLM_NETWORK_CATEGORY enumeration is a set of flags that specify the category type of a network.
helpviewer_keywords: ["NLM_NETWORK_CATEGORY","NLM_NETWORK_CATEGORY enumeration [Network Awareness]","NLM_NETWORK_CATEGORY_DOMAIN_AUTHENTICATED","NLM_NETWORK_CATEGORY_PRIVATE","NLM_NETWORK_CATEGORY_PUBLIC","netlistmgr/NLM_NETWORK_CATEGORY","netlistmgr/NLM_NETWORK_CATEGORY_DOMAIN_AUTHENTICATED","netlistmgr/NLM_NETWORK_CATEGORY_PRIVATE","netlistmgr/NLM_NETWORK_CATEGORY_PUBLIC","nla.nlm_network_category"]
old-location: nla\nlm_network_category.htm
tech.root: nla
ms.assetid: 1bc9720f-7b31-4a09-8bce-a6281ca9b9c4
ms.date: 12/05/2018
ms.keywords: NLM_NETWORK_CATEGORY, NLM_NETWORK_CATEGORY enumeration [Network Awareness], NLM_NETWORK_CATEGORY_DOMAIN_AUTHENTICATED, NLM_NETWORK_CATEGORY_PRIVATE, NLM_NETWORK_CATEGORY_PUBLIC, netlistmgr/NLM_NETWORK_CATEGORY, netlistmgr/NLM_NETWORK_CATEGORY_DOMAIN_AUTHENTICATED, netlistmgr/NLM_NETWORK_CATEGORY_PRIVATE, netlistmgr/NLM_NETWORK_CATEGORY_PUBLIC, nla.nlm_network_category
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
req.typenames: NLM_NETWORK_CATEGORY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NLM_NETWORK_CATEGORY
 - netlistmgr/NLM_NETWORK_CATEGORY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netlistmgr.h
api_name:
 - NLM_NETWORK_CATEGORY
---

# NLM_NETWORK_CATEGORY enumeration


## -description

The NLM_NETWORK_CATEGORY enumeration is  a set of flags that specify the category type of a network.

## -enum-fields

### -field NLM_NETWORK_CATEGORY_PUBLIC:0

The network is a public (untrusted) network.

### -field NLM_NETWORK_CATEGORY_PRIVATE:0x1

The network is a private (trusted) network.

### -field NLM_NETWORK_CATEGORY_DOMAIN_AUTHENTICATED:0x2

The network is authenticated against an Active Directory domain.

## -remarks

The private or public network categories must never be used to assume which Windows Firewall ports are open, as the user can change the default settings of these categories. Instead, Firewall APIs should be called to ensure the ports that the required ports are open.

