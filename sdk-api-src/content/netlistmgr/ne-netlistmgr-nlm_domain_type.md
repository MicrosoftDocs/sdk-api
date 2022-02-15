---
UID: NE:netlistmgr.NLM_DOMAIN_TYPE
title: NLM_DOMAIN_TYPE (netlistmgr.h)
description: The NLM_DOMAIN_TYPE enumeration is a set of flags that specify the domain type of a network.
helpviewer_keywords: ["NLM_DOMAIN_TYPE","NLM_DOMAIN_TYPE enumeration [Network Awareness]","NLM_DOMAIN_TYPE_DOMAIN_AUTHENTICATED","NLM_DOMAIN_TYPE_DOMAIN_NETWORK","NLM_DOMAIN_TYPE_NON_DOMAIN_NETWORK","netlistmgr/NLM_DOMAIN_TYPE","netlistmgr/NLM_DOMAIN_TYPE_DOMAIN_AUTHENTICATED","netlistmgr/NLM_DOMAIN_TYPE_DOMAIN_NETWORK","netlistmgr/NLM_DOMAIN_TYPE_NON_DOMAIN_NETWORK","nla.nlm_domain_type"]
old-location: nla\nlm_domain_type.htm
tech.root: nla
ms.assetid: fd1bc50a-c8d3-4594-870e-3bbb5c6ea1da
ms.date: 12/05/2018
ms.keywords: NLM_DOMAIN_TYPE, NLM_DOMAIN_TYPE enumeration [Network Awareness], NLM_DOMAIN_TYPE_DOMAIN_AUTHENTICATED, NLM_DOMAIN_TYPE_DOMAIN_NETWORK, NLM_DOMAIN_TYPE_NON_DOMAIN_NETWORK, netlistmgr/NLM_DOMAIN_TYPE, netlistmgr/NLM_DOMAIN_TYPE_DOMAIN_AUTHENTICATED, netlistmgr/NLM_DOMAIN_TYPE_DOMAIN_NETWORK, netlistmgr/NLM_DOMAIN_TYPE_NON_DOMAIN_NETWORK, nla.nlm_domain_type
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
req.typenames: NLM_DOMAIN_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NLM_DOMAIN_TYPE
 - netlistmgr/NLM_DOMAIN_TYPE
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
 - NLM_DOMAIN_TYPE
---

# NLM_DOMAIN_TYPE enumeration


## -description

The NLM_DOMAIN_TYPE enumeration is  a set of flags that specify the domain type of a network.

## -enum-fields

### -field NLM_DOMAIN_TYPE_NON_DOMAIN_NETWORK:0

The Network is not an Active Directory Network.

### -field NLM_DOMAIN_TYPE_DOMAIN_NETWORK:0x1

The Network is an Active Directory Network, but this machine is not authenticated against it.

### -field NLM_DOMAIN_TYPE_DOMAIN_AUTHENTICATED:0x2

The Network is an Active Directory Network, and this machine is authenticated against it.

