---
UID: NE:netlistmgr.NLM_NETWORK_PROPERTY_CHANGE
title: NLM_NETWORK_PROPERTY_CHANGE (netlistmgr.h)
description: The NLM_NETWORK_PROPERTY_CHANGE enumeration is a set of flags that define changes made to the properties of a network.
helpviewer_keywords: ["NLM_NETWORK_PROPERTY_CHANGE","NLM_NETWORK_PROPERTY_CHANGE enumeration [Network Awareness]","NLM_NETWORK_PROPERTY_CHANGE_CATEGORY_VALUE","NLM_NETWORK_PROPERTY_CHANGE_CONNECTION","NLM_NETWORK_PROPERTY_CHANGE_DESCRIPTION","NLM_NETWORK_PROPERTY_CHANGE_NAME","netlistmgr/NLM_NETWORK_PROPERTY_CHANGE","netlistmgr/NLM_NETWORK_PROPERTY_CHANGE_CATEGORY_VALUE","netlistmgr/NLM_NETWORK_PROPERTY_CHANGE_CONNECTION","netlistmgr/NLM_NETWORK_PROPERTY_CHANGE_DESCRIPTION","netlistmgr/NLM_NETWORK_PROPERTY_CHANGE_NAME","nla.nlm_network_property_change"]
old-location: nla\nlm_network_property_change.htm
tech.root: nla
ms.assetid: 04c96793-f6a8-418b-a8d4-65e8df77933c
ms.date: 12/05/2018
ms.keywords: NLM_NETWORK_PROPERTY_CHANGE, NLM_NETWORK_PROPERTY_CHANGE enumeration [Network Awareness], NLM_NETWORK_PROPERTY_CHANGE_CATEGORY_VALUE, NLM_NETWORK_PROPERTY_CHANGE_CONNECTION, NLM_NETWORK_PROPERTY_CHANGE_DESCRIPTION, NLM_NETWORK_PROPERTY_CHANGE_NAME, netlistmgr/NLM_NETWORK_PROPERTY_CHANGE, netlistmgr/NLM_NETWORK_PROPERTY_CHANGE_CATEGORY_VALUE, netlistmgr/NLM_NETWORK_PROPERTY_CHANGE_CONNECTION, netlistmgr/NLM_NETWORK_PROPERTY_CHANGE_DESCRIPTION, netlistmgr/NLM_NETWORK_PROPERTY_CHANGE_NAME, nla.nlm_network_property_change
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
req.typenames: NLM_NETWORK_PROPERTY_CHANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NLM_NETWORK_PROPERTY_CHANGE
 - netlistmgr/NLM_NETWORK_PROPERTY_CHANGE
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
 - NLM_NETWORK_PROPERTY_CHANGE
---

# NLM_NETWORK_PROPERTY_CHANGE enumeration


## -description

The NLM_NETWORK_PROPERTY_CHANGE enumeration is  a set of flags that define changes made to the properties of a network.

## -enum-fields

### -field NLM_NETWORK_PROPERTY_CHANGE_CONNECTION:0x1

A connection to this network has been added or removed.

### -field NLM_NETWORK_PROPERTY_CHANGE_DESCRIPTION:0x2

The description of the network has changed.

### -field NLM_NETWORK_PROPERTY_CHANGE_NAME:0x4

The name of the network has changed.

### -field NLM_NETWORK_PROPERTY_CHANGE_ICON:0x8

### -field NLM_NETWORK_PROPERTY_CHANGE_CATEGORY_VALUE:0x10

The category of the network has changed.

