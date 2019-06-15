---
UID: NE:clusapi._CLUSTER_SETUP_PHASE_SEVERITY
title: CLUSTER_SETUP_PHASE_SEVERITY (clusapi.h)
author: windows-sdk-content
description: Describes the severity of the current phase of the cluster setup process.
old-location: mscs\cluster_setup_phase_severity.htm
tech.root: MsCS
ms.assetid: a355dc8d-73f1-476b-a06f-24f011af4ace
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CLUSTER_SETUP_PHASE_SEVERITY, CLUSTER_SETUP_PHASE_SEVERITY enumeration [Failover Cluster], ClusterSetupPhaseFatal, ClusterSetupPhaseInformational, ClusterSetupPhaseWarning, clusapi/CLUSTER_SETUP_PHASE_SEVERITY, clusapi/ClusterSetupPhaseFatal, clusapi/ClusterSetupPhaseInformational, clusapi/ClusterSetupPhaseWarning, mscs.cluster_setup_phase_severity
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSTER_SETUP_PHASE_SEVERITY
product: Windows
targetos: Windows
req.typenames: CLUSTER_SETUP_PHASE_SEVERITY
req.redist: 
ms.custom: 19H1
---

# CLUSTER_SETUP_PHASE_SEVERITY enumeration


## -description


Describes the severity of the current phase of the cluster setup process. The 
    <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nc-clusapi-pcluster_setup_progress_callback">ClusterSetupProgressCallback</a> function 
    uses this enumeration.


## -enum-fields




### -field ClusterSetupPhaseInformational

This phase of the cluster setup can complete successfully.


### -field ClusterSetupPhaseWarning

This phase of the cluster setup can complete, with a warning.


### -field ClusterSetupPhaseFatal

This phase of the cluster setup process cannot complete successfully.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nc-clusapi-pcluster_setup_progress_callback">PCLUSTER_SETUP_PROGRESS_CALLBACK</a>
 

 

