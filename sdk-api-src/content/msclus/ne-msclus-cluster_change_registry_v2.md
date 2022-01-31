---
UID: NE:msclus.CLUSTER_CHANGE_REGISTRY_V2
title: CLUSTER_CHANGE_REGISTRY_V2 (msclus.h)
description: Defines the notifications that are generated for a registry key.
helpviewer_keywords: ["CLUSTER_CHANGE_REGISTRY_ALL_V2","CLUSTER_CHANGE_REGISTRY_ATTRIBUTES_V2","CLUSTER_CHANGE_REGISTRY_HANDLE_CLOSE_V2","CLUSTER_CHANGE_REGISTRY_NAME_V2","CLUSTER_CHANGE_REGISTRY_SUBTREE_V2","CLUSTER_CHANGE_REGISTRY_V2","CLUSTER_CHANGE_REGISTRY_V2 enumeration [Failover Cluster]","CLUSTER_CHANGE_REGISTRY_VALUE_V2","clusapi/CLUSTER_CHANGE_REGISTRY_ALL_V2","clusapi/CLUSTER_CHANGE_REGISTRY_ATTRIBUTES_V2","clusapi/CLUSTER_CHANGE_REGISTRY_HANDLE_CLOSE_V2","clusapi/CLUSTER_CHANGE_REGISTRY_NAME_V2","clusapi/CLUSTER_CHANGE_REGISTRY_SUBTREE_V2","clusapi/CLUSTER_CHANGE_REGISTRY_V2","clusapi/CLUSTER_CHANGE_REGISTRY_VALUE_V2","msclus/CLUSTER_CHANGE_REGISTRY_ALL_V2","msclus/CLUSTER_CHANGE_REGISTRY_ATTRIBUTES_V2","msclus/CLUSTER_CHANGE_REGISTRY_HANDLE_CLOSE_V2","msclus/CLUSTER_CHANGE_REGISTRY_NAME_V2","msclus/CLUSTER_CHANGE_REGISTRY_SUBTREE_V2","msclus/CLUSTER_CHANGE_REGISTRY_V2","msclus/CLUSTER_CHANGE_REGISTRY_VALUE_V2","mscs.cluster_change_registry_v2"]
old-location: mscs\cluster_change_registry_v2.htm
tech.root: MsCS
ms.assetid: 830A866B-D260-406B-B8E7-651F5149078E
ms.date: 12/05/2018
ms.keywords: CLUSTER_CHANGE_REGISTRY_ALL_V2, CLUSTER_CHANGE_REGISTRY_ATTRIBUTES_V2, CLUSTER_CHANGE_REGISTRY_HANDLE_CLOSE_V2, CLUSTER_CHANGE_REGISTRY_NAME_V2, CLUSTER_CHANGE_REGISTRY_SUBTREE_V2, CLUSTER_CHANGE_REGISTRY_V2, CLUSTER_CHANGE_REGISTRY_V2 enumeration [Failover Cluster], CLUSTER_CHANGE_REGISTRY_VALUE_V2, clusapi/CLUSTER_CHANGE_REGISTRY_ALL_V2, clusapi/CLUSTER_CHANGE_REGISTRY_ATTRIBUTES_V2, clusapi/CLUSTER_CHANGE_REGISTRY_HANDLE_CLOSE_V2, clusapi/CLUSTER_CHANGE_REGISTRY_NAME_V2, clusapi/CLUSTER_CHANGE_REGISTRY_SUBTREE_V2, clusapi/CLUSTER_CHANGE_REGISTRY_V2, clusapi/CLUSTER_CHANGE_REGISTRY_VALUE_V2, msclus/CLUSTER_CHANGE_REGISTRY_ALL_V2, msclus/CLUSTER_CHANGE_REGISTRY_ATTRIBUTES_V2, msclus/CLUSTER_CHANGE_REGISTRY_HANDLE_CLOSE_V2, msclus/CLUSTER_CHANGE_REGISTRY_NAME_V2, msclus/CLUSTER_CHANGE_REGISTRY_SUBTREE_V2, msclus/CLUSTER_CHANGE_REGISTRY_V2, msclus/CLUSTER_CHANGE_REGISTRY_VALUE_V2, mscs.cluster_change_registry_v2
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CLUSTER_CHANGE_REGISTRY_V2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_CHANGE_REGISTRY_V2
 - msclus/CLUSTER_CHANGE_REGISTRY_V2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUSTER_CHANGE_REGISTRY_V2
---

# CLUSTER_CHANGE_REGISTRY_V2 enumeration


## -description

Defines the notifications that are generated for a registry key.

## -enum-fields

### -field CLUSTER_CHANGE_REGISTRY_ATTRIBUTES_V2:0x1

Indicates that the registry attributes changed.

### -field CLUSTER_CHANGE_REGISTRY_NAME_V2:0x2

Indicates that the registry key name has changed.

### -field CLUSTER_CHANGE_REGISTRY_SUBTREE_V2:0x4

Indicates that the registry subtree has changed.

### -field CLUSTER_CHANGE_REGISTRY_VALUE_V2:0x8

Indicates that the registry value has changed.

### -field CLUSTER_CHANGE_REGISTRY_HANDLE_CLOSE_V2:0x10

Indicates that the registry's context handle was closed.

### -field CLUSTER_CHANGE_REGISTRY_ALL_V2

Indicates all V2 registry notifications.

## -remarks

Protocol version 2.0 servers do not support this enumeration.

