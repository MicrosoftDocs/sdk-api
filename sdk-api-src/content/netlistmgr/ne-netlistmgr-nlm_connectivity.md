---
UID: NE:netlistmgr.NLM_CONNECTIVITY
title: NLM_CONNECTIVITY (netlistmgr.h)
description: The NLM_Connectivity enumeration is a set of flags that provide notification whenever connectivity related parameters have changed.
helpviewer_keywords: ["NLM_CONNECTIVITY","NLM_CONNECTIVITY enumeration [Network Awareness]","NLM_CONNECTIVITY_DISCONNECTED","NLM_CONNECTIVITY_IPV4_INTERNET","NLM_CONNECTIVITY_IPV4_LOCALNETWORK","NLM_CONNECTIVITY_IPV4_NOTRAFFIC","NLM_CONNECTIVITY_IPV4_SUBNET","NLM_CONNECTIVITY_IPV6_INTERNET","NLM_CONNECTIVITY_IPV6_LOCALNETWORK","NLM_CONNECTIVITY_IPV6_NOTRAFFIC","NLM_CONNECTIVITY_IPV6_SUBNET","netlistmgr/NLM_CONNECTIVITY","netlistmgr/NLM_CONNECTIVITY_DISCONNECTED","netlistmgr/NLM_CONNECTIVITY_IPV4_INTERNET","netlistmgr/NLM_CONNECTIVITY_IPV4_LOCALNETWORK","netlistmgr/NLM_CONNECTIVITY_IPV4_NOTRAFFIC","netlistmgr/NLM_CONNECTIVITY_IPV4_SUBNET","netlistmgr/NLM_CONNECTIVITY_IPV6_INTERNET","netlistmgr/NLM_CONNECTIVITY_IPV6_LOCALNETWORK","netlistmgr/NLM_CONNECTIVITY_IPV6_NOTRAFFIC","netlistmgr/NLM_CONNECTIVITY_IPV6_SUBNET","nla.nlm_connectivity"]
old-location: nla\nlm_connectivity.htm
tech.root: nla
ms.assetid: 72d1f049-3c8d-4332-9bf1-9f49b47cd315
ms.date: 12/05/2018
ms.keywords: NLM_CONNECTIVITY, NLM_CONNECTIVITY enumeration [Network Awareness], NLM_CONNECTIVITY_DISCONNECTED, NLM_CONNECTIVITY_IPV4_INTERNET, NLM_CONNECTIVITY_IPV4_LOCALNETWORK, NLM_CONNECTIVITY_IPV4_NOTRAFFIC, NLM_CONNECTIVITY_IPV4_SUBNET, NLM_CONNECTIVITY_IPV6_INTERNET, NLM_CONNECTIVITY_IPV6_LOCALNETWORK, NLM_CONNECTIVITY_IPV6_NOTRAFFIC, NLM_CONNECTIVITY_IPV6_SUBNET, netlistmgr/NLM_CONNECTIVITY, netlistmgr/NLM_CONNECTIVITY_DISCONNECTED, netlistmgr/NLM_CONNECTIVITY_IPV4_INTERNET, netlistmgr/NLM_CONNECTIVITY_IPV4_LOCALNETWORK, netlistmgr/NLM_CONNECTIVITY_IPV4_NOTRAFFIC, netlistmgr/NLM_CONNECTIVITY_IPV4_SUBNET, netlistmgr/NLM_CONNECTIVITY_IPV6_INTERNET, netlistmgr/NLM_CONNECTIVITY_IPV6_LOCALNETWORK, netlistmgr/NLM_CONNECTIVITY_IPV6_NOTRAFFIC, netlistmgr/NLM_CONNECTIVITY_IPV6_SUBNET, nla.nlm_connectivity
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
req.typenames: NLM_CONNECTIVITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NLM_CONNECTIVITY
 - netlistmgr/NLM_CONNECTIVITY
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
 - NLM_CONNECTIVITY
---

# NLM_CONNECTIVITY enumeration


## -description

The NLM_Connectivity enumeration is  a set of flags that provide notification whenever connectivity related parameters have changed.

## -enum-fields

### -field NLM_CONNECTIVITY_DISCONNECTED:0

The underlying network interfaces have no connectivity to any network.

### -field NLM_CONNECTIVITY_IPV4_NOTRAFFIC:0x1

There is connectivity to a network, but the service cannot detect any IPv4 Network Traffic.

### -field NLM_CONNECTIVITY_IPV6_NOTRAFFIC:0x2

There is connectivity to a network, but the service cannot detect any IPv6 Network Traffic.

### -field NLM_CONNECTIVITY_IPV4_SUBNET:0x10

There is connectivity to the local subnet using the IPv4 protocol.

### -field NLM_CONNECTIVITY_IPV4_LOCALNETWORK:0x20

There is connectivity to a routed network using the IPv4 protocol.

### -field NLM_CONNECTIVITY_IPV4_INTERNET:0x40

There is connectivity to the Internet using the IPv4 protocol.

### -field NLM_CONNECTIVITY_IPV6_SUBNET:0x100

There is connectivity to the local subnet using the IPv6 protocol.

### -field NLM_CONNECTIVITY_IPV6_LOCALNETWORK:0x200

There is connectivity to a local network using the IPv6 protocol.

### -field NLM_CONNECTIVITY_IPV6_INTERNET:0x400

There is connectivity to the Internet using the IPv6 protocol.

