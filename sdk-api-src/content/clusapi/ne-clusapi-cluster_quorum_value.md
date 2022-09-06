---
UID: NE:clusapi.CLUSTER_QUORUM_VALUE
title: CLUSTER_QUORUM_VALUE (clusapi.h)
description: Enumerates values returned by the ClusterControl function with the CLUSCTL_CLUSTER_CHECK_VOTER_DOWN or the CLUSCTL_CLUSTER_CHECK_VOTER_EVICT control codes.
helpviewer_keywords: ["CLUSTER_QUORUM_LOST","CLUSTER_QUORUM_MAINTAINED","CLUSTER_QUORUM_VALUE","CLUSTER_QUORUM_VALUE enumeration [Failover Cluster]","msclus/CLUSTER_QUORUM_LOST","msclus/CLUSTER_QUORUM_MAINTAINED","msclus/CLUSTER_QUORUM_VALUE","mscs.cluster_quorum_value"]
old-location: mscs\cluster_quorum_value.htm
tech.root: MsCS
ms.assetid: 5b5310f5-b4f4-4c1e-82ad-3bbf3ebc511b
ms.date: 12/05/2018
ms.keywords: CLUSTER_QUORUM_LOST, CLUSTER_QUORUM_MAINTAINED, CLUSTER_QUORUM_VALUE, CLUSTER_QUORUM_VALUE enumeration [Failover Cluster], msclus/CLUSTER_QUORUM_LOST, msclus/CLUSTER_QUORUM_MAINTAINED, msclus/CLUSTER_QUORUM_VALUE, mscs.cluster_quorum_value
req.header: clusapi.h
req.include-header: ClusAPI.h
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
req.typenames: CLUSTER_QUORUM_VALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_QUORUM_VALUE
 - clusapi/CLUSTER_QUORUM_VALUE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msclus.h
api_name:
 - CLUSTER_QUORUM_VALUE
---

# CLUSTER_QUORUM_VALUE enumeration


## -description

Enumerates values returned by the 
    <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clustercontrol">ClusterControl</a> function with the 
    <a href="/previous-versions/windows/desktop/mscs/clusctl-cluster-check-voter-down">CLUSCTL_CLUSTER_CHECK_VOTER_DOWN</a> or the 
    <a href="/previous-versions/windows/desktop/mscs/clusctl-cluster-check-voter-evict">CLUSCTL_CLUSTER_CHECK_VOTER_EVICT</a> 
    control codes.

## -enum-fields

### -field CLUSTER_QUORUM_MAINTAINED:0

The quorum will be maintained.

### -field CLUSTER_QUORUM_LOST:1

The quorum will be lost.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-cluster-check-voter-down">CLUSCTL_CLUSTER_CHECK_VOTER_DOWN</a>



<a href="/previous-versions/windows/desktop/mscs/clusctl-cluster-check-voter-evict">CLUSCTL_CLUSTER_CHECK_VOTER_EVICT</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clustercontrol">ClusterControl</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
