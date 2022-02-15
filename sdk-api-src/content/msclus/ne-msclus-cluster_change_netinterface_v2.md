---
UID: NE:msclus.CLUSTER_CHANGE_NETINTERFACE_V2
title: CLUSTER_CHANGE_NETINTERFACE_V2 (msclus.h)
description: Defines the set of notifications that are generated for a cluster network interface.
helpviewer_keywords: ["CLUSTER_CHANGE_NETINTERFACE_ALL_V2","CLUSTER_CHANGE_NETINTERFACE_COMMON_PROPERTY_V2","CLUSTER_CHANGE_NETINTERFACE_DELETED_V2","CLUSTER_CHANGE_NETINTERFACE_HANDLE_CLOSE_V2","CLUSTER_CHANGE_NETINTERFACE_PRIVATE_PROPERTY_V2","CLUSTER_CHANGE_NETINTERFACE_STATE_V2","CLUSTER_CHANGE_NETINTERFACE_V2","CLUSTER_CHANGE_NETINTERFACE_V2 enumeration [Failover Cluster]","clusapi/CLUSTER_CHANGE_NETINTERFACE_ALL_V2","clusapi/CLUSTER_CHANGE_NETINTERFACE_COMMON_PROPERTY_V2","clusapi/CLUSTER_CHANGE_NETINTERFACE_DELETED_V2","clusapi/CLUSTER_CHANGE_NETINTERFACE_HANDLE_CLOSE_V2","clusapi/CLUSTER_CHANGE_NETINTERFACE_PRIVATE_PROPERTY_V2","clusapi/CLUSTER_CHANGE_NETINTERFACE_STATE_V2","clusapi/CLUSTER_CHANGE_NETINTERFACE_V2","msclus/CLUSTER_CHANGE_NETINTERFACE_ALL_V2","msclus/CLUSTER_CHANGE_NETINTERFACE_COMMON_PROPERTY_V2","msclus/CLUSTER_CHANGE_NETINTERFACE_DELETED_V2","msclus/CLUSTER_CHANGE_NETINTERFACE_HANDLE_CLOSE_V2","msclus/CLUSTER_CHANGE_NETINTERFACE_PRIVATE_PROPERTY_V2","msclus/CLUSTER_CHANGE_NETINTERFACE_STATE_V2","msclus/CLUSTER_CHANGE_NETINTERFACE_V2","mscs.cluster_change_netinterface_v2"]
old-location: mscs\cluster_change_netinterface_v2.htm
tech.root: MsCS
ms.assetid: E13FC26D-00D5-4E5A-8029-028AC04242EF
ms.date: 12/05/2018
ms.keywords: CLUSTER_CHANGE_NETINTERFACE_ALL_V2, CLUSTER_CHANGE_NETINTERFACE_COMMON_PROPERTY_V2, CLUSTER_CHANGE_NETINTERFACE_DELETED_V2, CLUSTER_CHANGE_NETINTERFACE_HANDLE_CLOSE_V2, CLUSTER_CHANGE_NETINTERFACE_PRIVATE_PROPERTY_V2, CLUSTER_CHANGE_NETINTERFACE_STATE_V2, CLUSTER_CHANGE_NETINTERFACE_V2, CLUSTER_CHANGE_NETINTERFACE_V2 enumeration [Failover Cluster], clusapi/CLUSTER_CHANGE_NETINTERFACE_ALL_V2, clusapi/CLUSTER_CHANGE_NETINTERFACE_COMMON_PROPERTY_V2, clusapi/CLUSTER_CHANGE_NETINTERFACE_DELETED_V2, clusapi/CLUSTER_CHANGE_NETINTERFACE_HANDLE_CLOSE_V2, clusapi/CLUSTER_CHANGE_NETINTERFACE_PRIVATE_PROPERTY_V2, clusapi/CLUSTER_CHANGE_NETINTERFACE_STATE_V2, clusapi/CLUSTER_CHANGE_NETINTERFACE_V2, msclus/CLUSTER_CHANGE_NETINTERFACE_ALL_V2, msclus/CLUSTER_CHANGE_NETINTERFACE_COMMON_PROPERTY_V2, msclus/CLUSTER_CHANGE_NETINTERFACE_DELETED_V2, msclus/CLUSTER_CHANGE_NETINTERFACE_HANDLE_CLOSE_V2, msclus/CLUSTER_CHANGE_NETINTERFACE_PRIVATE_PROPERTY_V2, msclus/CLUSTER_CHANGE_NETINTERFACE_STATE_V2, msclus/CLUSTER_CHANGE_NETINTERFACE_V2, mscs.cluster_change_netinterface_v2
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
req.typenames: CLUSTER_CHANGE_NETINTERFACE_V2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_CHANGE_NETINTERFACE_V2
 - msclus/CLUSTER_CHANGE_NETINTERFACE_V2
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
 - CLUSTER_CHANGE_NETINTERFACE_V2
---

# CLUSTER_CHANGE_NETINTERFACE_V2 enumeration


## -description

Defines the set of notifications that are generated for a cluster network interface.

## -enum-fields

### -field CLUSTER_CHANGE_NETINTERFACE_DELETED_V2:0x1

Indicates that the cluster network interface has been deleted.

### -field CLUSTER_CHANGE_NETINTERFACE_COMMON_PROPERTY_V2:0x2

Indicates that the common properties for the cluster interface have changed.

### -field CLUSTER_CHANGE_NETINTERFACE_PRIVATE_PROPERTY_V2:0x4

Indicates that the private properties for the cluster interface have changed.

### -field CLUSTER_CHANGE_NETINTERFACE_STATE_V2:0x8

Indicates that the state of the cluster interface has changed.

### -field CLUSTER_CHANGE_NETINTERFACE_HANDLE_CLOSE_V2:0x10

Indicates that the cluster interface's context handle was closed.

### -field CLUSTER_CHANGE_NETINTERFACE_ALL_V2

Indicates all V2 network interface notifications.

## -remarks

Protocol version 2.0 servers do not support this enumeration.

