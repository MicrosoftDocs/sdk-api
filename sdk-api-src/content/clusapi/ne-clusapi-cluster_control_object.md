---
UID: NE:clusapi.CLUSTER_CONTROL_OBJECT
title: CLUSTER_CONTROL_OBJECT (clusapi.h)
description: The 8-bit object component of a control code that indicates the type of cluster object to which the control code applies. For more information, see Control Code Architecture.
helpviewer_keywords: ["CLUSTER_CONTROL_OBJECT","CLUSTER_CONTROL_OBJECT enumeration [Failover Cluster]","CLUS_OBJECT_CLUSTER","CLUS_OBJECT_GROUP","CLUS_OBJECT_GROUPSET","CLUS_OBJECT_INVALID","CLUS_OBJECT_NETINTERFACE","CLUS_OBJECT_NETWORK","CLUS_OBJECT_NODE","CLUS_OBJECT_RESOURCE","CLUS_OBJECT_RESOURCE_TYPE","CLUS_OBJECT_USER","_CLUSTER_CONTROL_OBJECT","_CLUSTER_CONTROL_OBJECT enumeration [Failover Cluster]","clusapi/CLUSTER_CONTROL_OBJECT","clusapi/CLUS_OBJECT_CLUSTER","clusapi/CLUS_OBJECT_GROUP","clusapi/CLUS_OBJECT_GROUPSET","clusapi/CLUS_OBJECT_INVALID","clusapi/CLUS_OBJECT_NETINTERFACE","clusapi/CLUS_OBJECT_NETWORK","clusapi/CLUS_OBJECT_NODE","clusapi/CLUS_OBJECT_RESOURCE","clusapi/CLUS_OBJECT_RESOURCE_TYPE","clusapi/CLUS_OBJECT_USER","clusapi/_CLUSTER_CONTROL_OBJECT","msclus/CLUSTER_CONTROL_OBJECT","msclus/CLUS_OBJECT_CLUSTER","msclus/CLUS_OBJECT_GROUP","msclus/CLUS_OBJECT_GROUPSET","msclus/CLUS_OBJECT_INVALID","msclus/CLUS_OBJECT_NETINTERFACE","msclus/CLUS_OBJECT_NETWORK","msclus/CLUS_OBJECT_NODE","msclus/CLUS_OBJECT_RESOURCE","msclus/CLUS_OBJECT_RESOURCE_TYPE","msclus/CLUS_OBJECT_USER","msclus/_CLUSTER_CONTROL_OBJECT","mscs.cluster_control_object"]
old-location: mscs\cluster_control_object.htm
tech.root: MsCS
ms.assetid: 63719776-0b3a-470a-a732-40e62064c6fc
ms.date: 12/05/2018
ms.keywords: CLUSTER_CONTROL_OBJECT, CLUSTER_CONTROL_OBJECT enumeration [Failover Cluster], CLUS_OBJECT_CLUSTER, CLUS_OBJECT_GROUP, CLUS_OBJECT_GROUPSET, CLUS_OBJECT_INVALID, CLUS_OBJECT_NETINTERFACE, CLUS_OBJECT_NETWORK, CLUS_OBJECT_NODE, CLUS_OBJECT_RESOURCE, CLUS_OBJECT_RESOURCE_TYPE, CLUS_OBJECT_USER, _CLUSTER_CONTROL_OBJECT, _CLUSTER_CONTROL_OBJECT enumeration [Failover Cluster], clusapi/CLUSTER_CONTROL_OBJECT, clusapi/CLUS_OBJECT_CLUSTER, clusapi/CLUS_OBJECT_GROUP, clusapi/CLUS_OBJECT_GROUPSET, clusapi/CLUS_OBJECT_INVALID, clusapi/CLUS_OBJECT_NETINTERFACE, clusapi/CLUS_OBJECT_NETWORK, clusapi/CLUS_OBJECT_NODE, clusapi/CLUS_OBJECT_RESOURCE, clusapi/CLUS_OBJECT_RESOURCE_TYPE, clusapi/CLUS_OBJECT_USER, clusapi/_CLUSTER_CONTROL_OBJECT, msclus/CLUSTER_CONTROL_OBJECT, msclus/CLUS_OBJECT_CLUSTER, msclus/CLUS_OBJECT_GROUP, msclus/CLUS_OBJECT_GROUPSET, msclus/CLUS_OBJECT_INVALID, msclus/CLUS_OBJECT_NETINTERFACE, msclus/CLUS_OBJECT_NETWORK, msclus/CLUS_OBJECT_NODE, msclus/CLUS_OBJECT_RESOURCE, msclus/CLUS_OBJECT_RESOURCE_TYPE, msclus/CLUS_OBJECT_USER, msclus/_CLUSTER_CONTROL_OBJECT, mscs.cluster_control_object
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
req.typenames: CLUSTER_CONTROL_OBJECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_CONTROL_OBJECT
 - clusapi/CLUSTER_CONTROL_OBJECT
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
 - CLUSTER_CONTROL_OBJECT
---

# CLUSTER_CONTROL_OBJECT enumeration


## -description

The 8-bit object component of a control code that indicates the type of cluster object to which the 
    control code applies. For more information, see 
    <a href="/previous-versions/windows/desktop/mscs/control-code-architecture">Control Code Architecture</a>.

## -enum-fields

### -field CLUS_OBJECT_INVALID:0

Zero is not a valid object code value.

### -field CLUS_OBJECT_RESOURCE

Object code part of <a href="/previous-versions/windows/desktop/mscs/resource-control-codes">resource control codes</a> 
       that identifies cluster <a href="/previous-versions/windows/desktop/mscs/resources">resources</a> as the target.

### -field CLUS_OBJECT_RESOURCE_TYPE

Object code part of 
       <a href="/previous-versions/windows/desktop/mscs/resource-type-control-codes">resource type control codes</a> that identifies 
       cluster <a href="/previous-versions/windows/desktop/mscs/resource-types">resource types</a> as the target.

### -field CLUS_OBJECT_GROUP

Object code part of 
       <a href="/previous-versions/windows/desktop/mscs/group-control-codes">group control codes</a> that identifies cluster 
        <a href="/previous-versions/windows/desktop/mscs/groups">groups</a> as the target.

### -field CLUS_OBJECT_NODE

Object code part of <a href="/previous-versions/windows/desktop/mscs/node-control-codes">node control codes</a> that 
       identifies cluster <a href="/previous-versions/windows/desktop/mscs/nodes">nodes</a> as the target.

### -field CLUS_OBJECT_NETWORK

Object code part of <a href="/previous-versions/windows/desktop/mscs/network-control-codes">network control codes</a> that 
       identifies cluster <a href="/previous-versions/windows/desktop/mscs/networks">networks</a> as the target.

### -field CLUS_OBJECT_NETINTERFACE

Object code part of 
       <a href="/previous-versions/windows/desktop/mscs/network-interface-control-codes">network interface control codes</a> that 
       identifies cluster <a href="/previous-versions/windows/desktop/mscs/network-interfaces">network interfaces</a> as the 
       target.

### -field CLUS_OBJECT_CLUSTER

Object code part of <a href="/previous-versions/windows/desktop/mscs/cluster-control-codes">cluster control codes</a> that 
       identifies a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> as the target.

### -field CLUS_OBJECT_GROUPSET

Object code part of <a href="/previous-versions/windows/desktop/mscs/cluster-control-codes">cluster control codes</a> that 
       identifies a groupset as the target.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This constant is not supported prior to Windows Server 2016.

### -field CLUS_OBJECT_USER:128

Object code part of <a href="/previous-versions/windows/desktop/mscs/control-codes">control codes</a> that identifies 
       cluster object types not defined by Windows Clustering.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
