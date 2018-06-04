---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

