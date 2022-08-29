---
UID: NS:msclus._CLUSTER_MEMBERSHIP_INFO
title: CLUSTER_MEMBERSHIP_INFO (msclus.h)
description: The CLUSTER_MEMBERSHIP_INFO structure represents membership information for a cluster. (CLUSTER_MEMBERSHIP_INFO)
helpviewer_keywords: ["*PCLUSTER_MEMBERSHIP_INFO","CLUSTER_MEMBERSHIP_INFO","CLUSTER_MEMBERSHIP_INFO structure [Failover Cluster]","PCLUSTER_MEMBERSHIP_INFO","PCLUSTER_MEMBERSHIP_INFO structure pointer [Failover Cluster]","_CLUSTER_MEMBERSHIP_INFO","_CLUSTER_MEMBERSHIP_INFO structure [Failover Cluster]","clusapi/CLUSTER_MEMBERSHIP_INFO","clusapi/PCLUSTER_MEMBERSHIP_INFO","clusapi/_CLUSTER_MEMBERSHIP_INFO","msclus/CLUSTER_MEMBERSHIP_INFO","msclus/PCLUSTER_MEMBERSHIP_INFO","msclus/_CLUSTER_MEMBERSHIP_INFO","mscs.cluster_membership_info"]
old-location: mscs\cluster_membership_info.htm
tech.root: MsCS
ms.assetid: 4E3F8DFF-6F32-4729-9AAC-56B3E2592393
ms.date: 08/02/2022
ms.keywords: '*PCLUSTER_MEMBERSHIP_INFO, CLUSTER_MEMBERSHIP_INFO, CLUSTER_MEMBERSHIP_INFO structure [Failover Cluster], PCLUSTER_MEMBERSHIP_INFO, PCLUSTER_MEMBERSHIP_INFO structure pointer [Failover Cluster], _CLUSTER_MEMBERSHIP_INFO, _CLUSTER_MEMBERSHIP_INFO structure [Failover Cluster], clusapi/CLUSTER_MEMBERSHIP_INFO, clusapi/PCLUSTER_MEMBERSHIP_INFO, clusapi/_CLUSTER_MEMBERSHIP_INFO, msclus/CLUSTER_MEMBERSHIP_INFO, msclus/PCLUSTER_MEMBERSHIP_INFO, msclus/_CLUSTER_MEMBERSHIP_INFO, mscs.cluster_membership_info'
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
req.typenames: CLUSTER_MEMBERSHIP_INFO, *PCLUSTER_MEMBERSHIP_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSTER_MEMBERSHIP_INFO
 - msclus/_CLUSTER_MEMBERSHIP_INFO
 - PCLUSTER_MEMBERSHIP_INFO
 - msclus/PCLUSTER_MEMBERSHIP_INFO
 - CLUSTER_MEMBERSHIP_INFO
 - msclus/CLUSTER_MEMBERSHIP_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusApi.h
 - MsClus.h
api_name:
 - CLUSTER_MEMBERSHIP_INFO
---

# CLUSTER_MEMBERSHIP_INFO structure


## -description

Represents membership information for a cluster.

## -struct-fields

### -field HasQuorum

<b>TRUE</b> if the cluster has a majority quorum; otherwise <b>FALSE</b>.

### -field UpnodesSize

The size of the <i>Upnodes</i> parameter.

### -field Upnodes

A byte array that specifies the nodes in the cluster that are online.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/data-structures">Data Structures</a>
