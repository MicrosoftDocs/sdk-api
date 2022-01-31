---
UID: NE:msclus.CLUSTER_RESOURCE_CLASS
title: CLUSTER_RESOURCE_CLASS (msclus.h)
description: Defines the class of a resource.
helpviewer_keywords: ["CLUSTER_RESOURCE_CLASS","CLUSTER_RESOURCE_CLASS enumeration [Failover Cluster]","CLUS_RESCLASS_NETWORK","CLUS_RESCLASS_STORAGE","CLUS_RESCLASS_UNKNOWN","CLUS_RESCLASS_USER","_CLUSTER_RESOURCE_CLASS","_CLUSTER_RESOURCE_CLASS enumeration [Failover Cluster]","clusapi/CLUSTER_RESOURCE_CLASS","clusapi/CLUS_RESCLASS_NETWORK","clusapi/CLUS_RESCLASS_STORAGE","clusapi/CLUS_RESCLASS_UNKNOWN","clusapi/CLUS_RESCLASS_USER","clusapi/_CLUSTER_RESOURCE_CLASS","msclus/CLUSTER_RESOURCE_CLASS","msclus/CLUS_RESCLASS_NETWORK","msclus/CLUS_RESCLASS_STORAGE","msclus/CLUS_RESCLASS_UNKNOWN","msclus/CLUS_RESCLASS_USER","msclus/_CLUSTER_RESOURCE_CLASS","mscs.cluster_resource_class"]
old-location: mscs\cluster_resource_class.htm
tech.root: MsCS
ms.assetid: 65168256-f097-48a5-9e86-ec419ccb13bd
ms.date: 12/05/2018
ms.keywords: CLUSTER_RESOURCE_CLASS, CLUSTER_RESOURCE_CLASS enumeration [Failover Cluster], CLUS_RESCLASS_NETWORK, CLUS_RESCLASS_STORAGE, CLUS_RESCLASS_UNKNOWN, CLUS_RESCLASS_USER, _CLUSTER_RESOURCE_CLASS, _CLUSTER_RESOURCE_CLASS enumeration [Failover Cluster], clusapi/CLUSTER_RESOURCE_CLASS, clusapi/CLUS_RESCLASS_NETWORK, clusapi/CLUS_RESCLASS_STORAGE, clusapi/CLUS_RESCLASS_UNKNOWN, clusapi/CLUS_RESCLASS_USER, clusapi/_CLUSTER_RESOURCE_CLASS, msclus/CLUSTER_RESOURCE_CLASS, msclus/CLUS_RESCLASS_NETWORK, msclus/CLUS_RESCLASS_STORAGE, msclus/CLUS_RESCLASS_UNKNOWN, msclus/CLUS_RESCLASS_USER, msclus/_CLUSTER_RESOURCE_CLASS, mscs.cluster_resource_class
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
req.typenames: CLUSTER_RESOURCE_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_RESOURCE_CLASS
 - msclus/CLUSTER_RESOURCE_CLASS
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
 - CLUSTER_RESOURCE_CLASS
---

# CLUSTER_RESOURCE_CLASS enumeration


## -description

Defines the class of a resource.

## -enum-fields

### -field CLUS_RESCLASS_UNKNOWN:0

Resource class is unknown.

### -field CLUS_RESCLASS_STORAGE

Resource is a storage device, such as a 
           <a href="/previous-versions/windows/desktop/mscs/p-gly">Physical Disk resource</a>.

### -field CLUS_RESCLASS_NETWORK

Resource is a <a href="/previous-versions/windows/desktop/mscs/n-gly">network</a> device.

### -field CLUS_RESCLASS_USER:32768

Resource classes beginning at this value are user-defined.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_resource_class_info">CLUS_RESOURCE_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/mscs/clusresource-classinfo">ClassInfo Property of the ClusResource Object</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
