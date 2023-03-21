---
UID: NE:netlistmgr.NLM_NETWORK_CLASS
title: NLM_NETWORK_CLASS (netlistmgr.h)
description: NLM_NETWORK_CLASS enumeration defines a set of flags that specify if a network has been identified.
helpviewer_keywords: ["NLM_NETWORK_CLASS","NLM_NETWORK_CLASS enumeration [Network Awareness]","NLM_NETWORK_IDENTIFIED","NLM_NETWORK_IDENTIFYING","NLM_NETWORK_UNIDENTIFIED","netlistmgr/NLM_NETWORK_CLASS","netlistmgr/NLM_NETWORK_IDENTIFIED","netlistmgr/NLM_NETWORK_IDENTIFYING","netlistmgr/NLM_NETWORK_UNIDENTIFIED","nla.nlm_network_class"]
old-location: nla\nlm_network_class.htm
tech.root: nla
ms.assetid: 397602c6-efc5-454a-999b-26ea26cb56cd
ms.date: 12/05/2018
ms.keywords: NLM_NETWORK_CLASS, NLM_NETWORK_CLASS enumeration [Network Awareness], NLM_NETWORK_IDENTIFIED, NLM_NETWORK_IDENTIFYING, NLM_NETWORK_UNIDENTIFIED, netlistmgr/NLM_NETWORK_CLASS, netlistmgr/NLM_NETWORK_IDENTIFIED, netlistmgr/NLM_NETWORK_IDENTIFYING, netlistmgr/NLM_NETWORK_UNIDENTIFIED, nla.nlm_network_class
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
req.typenames: NLM_NETWORK_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NLM_NETWORK_CLASS
 - netlistmgr/NLM_NETWORK_CLASS
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
 - NLM_NETWORK_CLASS
---

# NLM_NETWORK_CLASS enumeration


## -description

The <b>NLM_NETWORK_CLASS</b> enumeration defines a set of flags that specify if a network has been identified.

## -enum-fields

### -field NLM_NETWORK_IDENTIFYING:0x1

The network is being identified.

### -field NLM_NETWORK_IDENTIFIED:0x2

The network has been identified.

### -field NLM_NETWORK_UNIDENTIFIED:0x3

The network has not been identified.

