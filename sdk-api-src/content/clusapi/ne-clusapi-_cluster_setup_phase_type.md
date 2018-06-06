---
UID: NE:clusapi._CLUSTER_SETUP_PHASE_TYPE
title: "_CLUSTER_SETUP_PHASE_TYPE"
author: windows-sdk-content
description: Describes the progress of the cluster setup process.
old-location: mscs\cluster_setup_phase_type.htm
old-project: MsCS
ms.assetid: 515fe36d-84a0-41f1-80fa-a8c12718bdf5
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: CLUSTER_SETUP_PHASE_TYPE, CLUSTER_SETUP_PHASE_TYPE enumeration [Failover Cluster], ClusterSetupPhaseContinue, ClusterSetupPhaseEnd, ClusterSetupPhaseStart, _CLUSTER_SETUP_PHASE_TYPE, clusapi/CLUSTER_SETUP_PHASE_TYPE, clusapi/ClusterSetupPhaseContinue, clusapi/ClusterSetupPhaseEnd, clusapi/ClusterSetupPhaseStart, mscs.cluster_setup_phase_type
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
req.typenames: CLUSTER_SETUP_PHASE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSTER_SETUP_PHASE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CLUSTER_SETUP_PHASE_TYPE enumeration


## -description


Describes the  progress of the cluster setup process. The 
    <a href="https://msdn.microsoft.com/fb7a6991-576c-4c03-aef0-89811fbc1a0d">ClusterSetupProgressCallback</a> function 
    uses this enumeration. The values of the 
    <a href="https://msdn.microsoft.com/cc881b92-c312-4b88-8d8d-09f98925b5b5">CLUSTER_SETUP_PHASE</a> enumeration identify the current 
    phase of the cluster setup process. The values of the 
    <a href="https://msdn.microsoft.com/a355dc8d-73f1-476b-a06f-24f011af4ace">CLUSTER_SETUP_PHASE_SEVERITY</a> enumeration 
    describe the  severity of the cluster setup process.


## -enum-fields




### -field ClusterSetupPhaseStart

Indicates the start of a new setup phase.


### -field ClusterSetupPhaseContinue

Indicates the continuation of a setup phase.


### -field ClusterSetupPhaseEnd

Indicates the end of a setup phase. Called once at the end of every setup phase.


### -field ClusterSetupPhaseReport




## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/fb7a6991-576c-4c03-aef0-89811fbc1a0d">PCLUSTER_SETUP_PROGRESS_CALLBACK</a>
 

 

