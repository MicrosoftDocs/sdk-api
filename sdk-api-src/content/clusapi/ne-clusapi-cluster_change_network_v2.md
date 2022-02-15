---
UID: NE:clusapi.CLUSTER_CHANGE_NETWORK_V2
title: CLUSTER_CHANGE_NETWORK_V2 (clusapi.h)
description: Defines the notifications that are generated for a cluster network.
helpviewer_keywords: ["CLUSTER_CHANGE_NETWORK_ALL_V2","CLUSTER_CHANGE_NETWORK_COMMON_PROPERTY_V2","CLUSTER_CHANGE_NETWORK_DELETED_V2","CLUSTER_CHANGE_NETWORK_HANDLE_CLOSE_V2","CLUSTER_CHANGE_NETWORK_PRIVATE_PROPERTY_V2","CLUSTER_CHANGE_NETWORK_STATE_V2","CLUSTER_CHANGE_NETWORK_V2","CLUSTER_CHANGE_NETWORK_V2 enumeration [Failover Cluster]","clusapi/CLUSTER_CHANGE_NETWORK_ALL_V2","clusapi/CLUSTER_CHANGE_NETWORK_COMMON_PROPERTY_V2","clusapi/CLUSTER_CHANGE_NETWORK_DELETED_V2","clusapi/CLUSTER_CHANGE_NETWORK_HANDLE_CLOSE_V2","clusapi/CLUSTER_CHANGE_NETWORK_PRIVATE_PROPERTY_V2","clusapi/CLUSTER_CHANGE_NETWORK_STATE_V2","clusapi/CLUSTER_CHANGE_NETWORK_V2","msclus/CLUSTER_CHANGE_NETWORK_ALL_V2","msclus/CLUSTER_CHANGE_NETWORK_COMMON_PROPERTY_V2","msclus/CLUSTER_CHANGE_NETWORK_DELETED_V2","msclus/CLUSTER_CHANGE_NETWORK_HANDLE_CLOSE_V2","msclus/CLUSTER_CHANGE_NETWORK_PRIVATE_PROPERTY_V2","msclus/CLUSTER_CHANGE_NETWORK_STATE_V2","msclus/CLUSTER_CHANGE_NETWORK_V2","mscs.cluster_change_network_v2"]
old-location: mscs\cluster_change_network_v2.htm
tech.root: MsCS
ms.assetid: 1FEB810F-C289-4615-8BCB-B1343200CBF1
ms.date: 12/05/2018
ms.keywords: CLUSTER_CHANGE_NETWORK_ALL_V2, CLUSTER_CHANGE_NETWORK_COMMON_PROPERTY_V2, CLUSTER_CHANGE_NETWORK_DELETED_V2, CLUSTER_CHANGE_NETWORK_HANDLE_CLOSE_V2, CLUSTER_CHANGE_NETWORK_PRIVATE_PROPERTY_V2, CLUSTER_CHANGE_NETWORK_STATE_V2, CLUSTER_CHANGE_NETWORK_V2, CLUSTER_CHANGE_NETWORK_V2 enumeration [Failover Cluster], clusapi/CLUSTER_CHANGE_NETWORK_ALL_V2, clusapi/CLUSTER_CHANGE_NETWORK_COMMON_PROPERTY_V2, clusapi/CLUSTER_CHANGE_NETWORK_DELETED_V2, clusapi/CLUSTER_CHANGE_NETWORK_HANDLE_CLOSE_V2, clusapi/CLUSTER_CHANGE_NETWORK_PRIVATE_PROPERTY_V2, clusapi/CLUSTER_CHANGE_NETWORK_STATE_V2, clusapi/CLUSTER_CHANGE_NETWORK_V2, msclus/CLUSTER_CHANGE_NETWORK_ALL_V2, msclus/CLUSTER_CHANGE_NETWORK_COMMON_PROPERTY_V2, msclus/CLUSTER_CHANGE_NETWORK_DELETED_V2, msclus/CLUSTER_CHANGE_NETWORK_HANDLE_CLOSE_V2, msclus/CLUSTER_CHANGE_NETWORK_PRIVATE_PROPERTY_V2, msclus/CLUSTER_CHANGE_NETWORK_STATE_V2, msclus/CLUSTER_CHANGE_NETWORK_V2, mscs.cluster_change_network_v2
req.header: clusapi.h
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
req.typenames: CLUSTER_CHANGE_NETWORK_V2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_CHANGE_NETWORK_V2
 - clusapi/CLUSTER_CHANGE_NETWORK_V2
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
 - CLUSTER_CHANGE_NETWORK_V2
---

# CLUSTER_CHANGE_NETWORK_V2 enumeration


## -description

Defines the notifications that are generated for a cluster network.

## -enum-fields

### -field CLUSTER_CHANGE_NETWORK_DELETED_V2:0x00000001

Indicates that the cluster network has been deleted.

### -field CLUSTER_CHANGE_NETWORK_COMMON_PROPERTY_V2:0x00000002

Indicates that the common properties for the cluster network have changed.

### -field CLUSTER_CHANGE_NETWORK_PRIVATE_PROPERTY_V2:0x00000004

Indicates that the private properties for the cluster network have changed.

### -field CLUSTER_CHANGE_NETWORK_STATE_V2:0x00000008

Indicates that the cluster network state has changed.

### -field CLUSTER_CHANGE_NETWORK_HANDLE_CLOSE_V2:0x00000010

Indicates that the cluster network's context handle was closed.

### -field CLUSTER_CHANGE_NETWORK_ALL_V2

Indicates all V2 cluster network notifications.

## -remarks

Protocol version 2.0 servers do not support this enumeration.

