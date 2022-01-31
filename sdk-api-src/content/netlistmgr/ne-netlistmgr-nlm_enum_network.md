---
UID: NE:netlistmgr.NLM_ENUM_NETWORK
title: NLM_ENUM_NETWORK (netlistmgr.h)
description: The NLM_ENUM_NETWORK enumeration contains a set of flags that specify what types of networks are enumerated.
helpviewer_keywords: ["NLM_ENUM_NETWORK","NLM_ENUM_NETWORK enumeration [Network Awareness]","NLM_ENUM_NETWORK_ALL","NLM_ENUM_NETWORK_CONNECTED","NLM_ENUM_NETWORK_DISCONNECTED","netlistmgr/NLM_ENUM_NETWORK","netlistmgr/NLM_ENUM_NETWORK_ALL","netlistmgr/NLM_ENUM_NETWORK_CONNECTED","netlistmgr/NLM_ENUM_NETWORK_DISCONNECTED","nla.nlm_enum_network"]
old-location: nla\nlm_enum_network.htm
tech.root: nla
ms.assetid: 37eb1e2e-d769-4e58-b93d-582312bd500a
ms.date: 12/05/2018
ms.keywords: NLM_ENUM_NETWORK, NLM_ENUM_NETWORK enumeration [Network Awareness], NLM_ENUM_NETWORK_ALL, NLM_ENUM_NETWORK_CONNECTED, NLM_ENUM_NETWORK_DISCONNECTED, netlistmgr/NLM_ENUM_NETWORK, netlistmgr/NLM_ENUM_NETWORK_ALL, netlistmgr/NLM_ENUM_NETWORK_CONNECTED, netlistmgr/NLM_ENUM_NETWORK_DISCONNECTED, nla.nlm_enum_network
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
req.typenames: NLM_ENUM_NETWORK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NLM_ENUM_NETWORK
 - netlistmgr/NLM_ENUM_NETWORK
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
 - NLM_ENUM_NETWORK
---

# NLM_ENUM_NETWORK enumeration


## -description

The NLM_ENUM_NETWORK enumeration  contains a set of flags that specify what types of networks are enumerated.

## -enum-fields

### -field NLM_ENUM_NETWORK_CONNECTED:0x1

Returns connected networks

### -field NLM_ENUM_NETWORK_DISCONNECTED:0x2

Returns disconnected networks

### -field NLM_ENUM_NETWORK_ALL:0x3

Returns connected and disconnected networks

