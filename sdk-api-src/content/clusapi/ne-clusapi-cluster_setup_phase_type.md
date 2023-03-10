---
UID: NE:clusapi._CLUSTER_SETUP_PHASE_TYPE
title: CLUSTER_SETUP_PHASE_TYPE (clusapi.h)
description: Describes the progress of the cluster setup process.
helpviewer_keywords: ["CLUSTER_SETUP_PHASE_TYPE","CLUSTER_SETUP_PHASE_TYPE enumeration [Failover Cluster]","ClusterSetupPhaseContinue","ClusterSetupPhaseEnd","ClusterSetupPhaseStart","clusapi/CLUSTER_SETUP_PHASE_TYPE","clusapi/ClusterSetupPhaseContinue","clusapi/ClusterSetupPhaseEnd","clusapi/ClusterSetupPhaseStart","mscs.cluster_setup_phase_type"]
old-location: mscs\cluster_setup_phase_type.htm
tech.root: MsCS
ms.assetid: 515fe36d-84a0-41f1-80fa-a8c12718bdf5
ms.date: 12/05/2018
ms.keywords: CLUSTER_SETUP_PHASE_TYPE, CLUSTER_SETUP_PHASE_TYPE enumeration [Failover Cluster], ClusterSetupPhaseContinue, ClusterSetupPhaseEnd, ClusterSetupPhaseStart, clusapi/CLUSTER_SETUP_PHASE_TYPE, clusapi/ClusterSetupPhaseContinue, clusapi/ClusterSetupPhaseEnd, clusapi/ClusterSetupPhaseStart, mscs.cluster_setup_phase_type
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
req.typenames: CLUSTER_SETUP_PHASE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSTER_SETUP_PHASE_TYPE
 - clusapi/_CLUSTER_SETUP_PHASE_TYPE
 - CLUSTER_SETUP_PHASE_TYPE
 - clusapi/CLUSTER_SETUP_PHASE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSTER_SETUP_PHASE_TYPE
---

# CLUSTER_SETUP_PHASE_TYPE enumeration


## -description

Describes the  progress of the cluster setup process. The 
    <a href="/windows/desktop/api/clusapi/nc-clusapi-pcluster_setup_progress_callback">ClusterSetupProgressCallback</a> function 
    uses this enumeration. The values of the 
    <a href="/windows/desktop/api/clusapi/ne-clusapi-cluster_setup_phase">CLUSTER_SETUP_PHASE</a> enumeration identify the current 
    phase of the cluster setup process. The values of the 
    <a href="/windows/desktop/api/clusapi/ne-clusapi-cluster_setup_phase_severity">CLUSTER_SETUP_PHASE_SEVERITY</a> enumeration 
    describe the  severity of the cluster setup process.

## -enum-fields

### -field ClusterSetupPhaseStart:1

Indicates the start of a new setup phase.

### -field ClusterSetupPhaseContinue:2

Indicates the continuation of a setup phase.

### -field ClusterSetupPhaseEnd:3

Indicates the end of a setup phase. Called once at the end of every setup phase.

### -field ClusterSetupPhaseReport:4

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="/windows/desktop/api/clusapi/nc-clusapi-pcluster_setup_progress_callback">PCLUSTER_SETUP_PROGRESS_CALLBACK</a>
