---
UID: NE:clusapi._CLUSTER_SETUP_PHASE_SEVERITY
title: "_CLUSTER_SETUP_PHASE_SEVERITY"
author: windows-sdk-content
description: Describes the severity of the current phase of the cluster setup process.
old-location: mscs\cluster_setup_phase_severity.htm
old-project: mscs
ms.assetid: a355dc8d-73f1-476b-a06f-24f011af4ace
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: CLUSTER_SETUP_PHASE_SEVERITY, CLUSTER_SETUP_PHASE_SEVERITY enumeration [Failover Cluster], ClusterSetupPhaseFatal, ClusterSetupPhaseInformational, ClusterSetupPhaseWarning, _CLUSTER_SETUP_PHASE_SEVERITY, clusapi/CLUSTER_SETUP_PHASE_SEVERITY, clusapi/ClusterSetupPhaseFatal, clusapi/ClusterSetupPhaseInformational, clusapi/ClusterSetupPhaseWarning, mscs.cluster_setup_phase_severity
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CLUSTER_SETUP_PHASE_SEVERITY
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
req.lib: 
req.dll: 
req.irql: 
---

# _CLUSTER_SETUP_PHASE_SEVERITY enumeration


## -description


Describes the severity of the current phase of the cluster setup process. The 
    <a href="https://msdn.microsoft.com/fb7a6991-576c-4c03-aef0-89811fbc1a0d">ClusterSetupProgressCallback</a> function 
    uses this enumeration.


## -enum-fields




### -field ClusterSetupPhaseInformational

This phase of the cluster setup can complete successfully.


### -field ClusterSetupPhaseWarning

This phase of the cluster setup can complete, with a warning.


### -field ClusterSetupPhaseFatal

This phase of the cluster setup process cannot complete successfully.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/fb7a6991-576c-4c03-aef0-89811fbc1a0d">PCLUSTER_SETUP_PROGRESS_CALLBACK</a>
 

 

