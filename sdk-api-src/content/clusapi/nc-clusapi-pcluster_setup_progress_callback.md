---
UID: NC:clusapi.PCLUSTER_SETUP_PROGRESS_CALLBACK
title: PCLUSTER_SETUP_PROGRESS_CALLBACK
author: windows-driver-content
description: Callback function that receives regular updates on the progression of the setup of the cluster.
old-location: mscs\pcluster_setup_progress_callback.htm
old-project: MsCS
ms.assetid: fb7a6991-576c-4c03-aef0-89811fbc1a0d
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ClusterSetupPhaseAddClusterProperties, ClusterSetupPhaseAddNodeToCluster, ClusterSetupPhaseCleanupCOs, ClusterSetupPhaseCleanupNode, ClusterSetupPhaseClusterGroupOnline, ClusterSetupPhaseConfigureClusSvc, ClusterSetupPhaseConfigureClusterAccount, ClusterSetupPhaseContinue, ClusterSetupPhaseCoreGroupCleanup, ClusterSetupPhaseCreateClusterAccount, ClusterSetupPhaseCreateGroups, ClusterSetupPhaseCreateIPAddressResources, ClusterSetupPhaseCreateNetworkName, ClusterSetupPhaseCreateResourceTypes, ClusterSetupPhaseDeleteGroup, ClusterSetupPhaseEnd, ClusterSetupPhaseEvictNode, ClusterSetupPhaseFailureCleanup, ClusterSetupPhaseFatal, ClusterSetupPhaseFormingCluster, ClusterSetupPhaseGettingCurrentMembership, ClusterSetupPhaseInformational, ClusterSetupPhaseInitialize, ClusterSetupPhaseMoveGroup, ClusterSetupPhaseNodeUp, ClusterSetupPhaseOfflineGroup, ClusterSetupPhaseQueryClusterNameAccount, ClusterSetupPhaseStart, ClusterSetupPhaseStartingClusSvc, ClusterSetupPhaseValidateClusDisk, ClusterSetupPhaseValidateClusterNameAccount, ClusterSetupPhaseValidateNetft, ClusterSetupPhaseValidateNodeState, ClusterSetupPhaseWarning, ClusterSetupProgressCallback, ClusterSetupProgressCallback callback function [Failover Cluster], PCLUSTER_SETUP_PROGRESS_CALLBACK, PCLUSTER_SETUP_PROGRESS_CALLBACK callback function [Failover Cluster], clusapi/ClusterSetupProgressCallback, clusapi/PCLUSTER_SETUP_PROGRESS_CALLBACK, mscs.pcluster_setup_progress_callback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: clusapi.h
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
req.typenames: Sources
topic_type:
-	kbSyntax
api_type:
-	<TBD>
api_location:
-
api_name:
-	ClusterSetupProgressCallback callback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSTER_SETUP_PROGRESS_CALLBACK callback


## -description


Callback function that receives regular updates on the progression of the setup of the 
    cluster. This callback is used during processing of the 
    <a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a>, 
    <a href="https://msdn.microsoft.com/e1d3611e-10d1-4858-923a-01633d2ed78b">AddClusterNode</a>, and 
    <a href="https://msdn.microsoft.com/55e601de-b427-43cd-b7f8-6cc576077e59">DestroyCluster</a> functions.


## -parameters




### -param pvCallbackArg [in, optional]

<i>pvCallbackArg</i> parameter passed to the 
       <a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a>, 
       <a href="https://msdn.microsoft.com/e1d3611e-10d1-4858-923a-01633d2ed78b">AddClusterNode</a>, or 
       <a href="https://msdn.microsoft.com/55e601de-b427-43cd-b7f8-6cc576077e59">DestroyCluster</a> function.


### -param eSetupPhase [in]

Value from the <a href="https://msdn.microsoft.com/cc881b92-c312-4b88-8d8d-09f98925b5b5">CLUSTER_SETUP_PHASE</a> enumeration 
       that gives the current setup phase. The parameter can be one of the following values.



#### ClusterSetupPhaseInitialize (1)

Initialize cluster setup.



#### ClusterSetupPhaseValidateNodeState (100)

Validate cluster nodes.



#### ClusterSetupPhaseValidateNetft (102)

Validate cluster networks.



#### ClusterSetupPhaseValidateClusDisk (103)

Validate cluster disks.



#### ClusterSetupPhaseConfigureClusSvc (104)

Configure cluster service.



#### ClusterSetupPhaseStartingClusSvc (105)

Start  cluster service.



#### ClusterSetupPhaseQueryClusterNameAccount (106)

Query cluster name.



#### ClusterSetupPhaseValidateClusterNameAccount (107)

Validate cluster name.



#### ClusterSetupPhaseCreateClusterAccount (108)

Create cluster account.



#### ClusterSetupPhaseConfigureClusterAccount (109)

Configure cluster account.



#### ClusterSetupPhaseFormingCluster (200)

Form the cluster.



#### ClusterSetupPhaseAddClusterProperties (201)

Add properties to cluster.



#### ClusterSetupPhaseCreateResourceTypes (202)

Create resource types.



#### ClusterSetupPhaseCreateGroups (203)

Create resource groups.



#### ClusterSetupPhaseCreateIPAddressResources (204)

Create IP address resources.



#### ClusterSetupPhaseCreateNetworkName (205)

Create network name.



#### ClusterSetupPhaseClusterGroupOnline (206)

Bring cluster groups online.



#### ClusterSetupPhaseGettingCurrentMembership (300)

Get current cluster membership.



#### ClusterSetupPhaseAddNodeToCluster (301)

Add node to cluster membership.



#### ClusterSetupPhaseNodeUp (302)

Start node.



#### ClusterSetupPhaseMoveGroup (400)

Move group to another node.



#### ClusterSetupPhaseDeleteGroup (401)

Delete group from cluster.



#### ClusterSetupPhaseCleanupCOs (402)

Clean up offline group.



#### ClusterSetupPhaseOfflineGroup (403)

Move group offline.



#### ClusterSetupPhaseEvictNode (404)

Remove a node from the cluster.



#### ClusterSetupPhaseCleanupNode (405)

Return node to pre-clustered state.



#### ClusterSetupPhaseCoreGroupCleanup (406)

Return core resource group to pre-clustered state.



#### ClusterSetupPhaseFailureCleanup (999)

Return failed resource to pre-clustered state.


### -param ePhaseType [in]

Value from the <a href="https://msdn.microsoft.com/515fe36d-84a0-41f1-80fa-a8c12718bdf5">CLUSTER_SETUP_PHASE_TYPE</a> 
       enumeration that gives the current setup phase type. The parameter can be one of the following values.



#### ClusterSetupPhaseStart (1)

Indicates the start of a new setup phase as passed in the <i>eSetupPhase</i> 
         parameter.



#### ClusterSetupPhaseContinue (2)

Indicates the continuation of a setup phase as passed in the <i>eSetupPhase</i> 
         parameter. This callback can be repeated during the processing of the specific setup phase and type.



#### ClusterSetupPhaseEnd (3)

Called once at the end of every setup phase as passed in the <i>eSetupPhase</i> 
         parameter.


### -param ePhaseSeverity [in]

Value from the 
       <a href="https://msdn.microsoft.com/a355dc8d-73f1-476b-a06f-24f011af4ace">CLUSTER_SETUP_PHASE_SEVERITY</a> enumeration 
       that gives the current setup phase severity. The parameter can be one of the following values.



#### ClusterSetupPhaseInformational (1)

This phase of the cluster setup can complete successfully.



#### ClusterSetupPhaseWarning (2)

This phase of the cluster setup can complete, with a warning.



#### ClusterSetupPhaseFatal (3)

This phase of the cluster setup process cannot complete successfully.


### -param dwPercentComplete [in]

Indicates approximate percentage of setup that has been completed.

Range: 0–100


### -param lpszObjectName [in, optional]

Name of the object.


### -param dwStatus [in]

Status


## -returns



TBD




## -remarks



The <b>PCLUSTER_SETUP_PROGRESS_CALLBACK</b> type defines a pointer to this function.

The <a href="https://msdn.microsoft.com/f6ff92b7-608f-423c-9977-364a8eb44cec">MSCluster_EventClusterCallback</a> 
     MOF class is used in a similar manner.




## -see-also




<a href="https://msdn.microsoft.com/e1d3611e-10d1-4858-923a-01633d2ed78b">AddClusterNode</a>



<a href="https://msdn.microsoft.com/cc881b92-c312-4b88-8d8d-09f98925b5b5">CLUSTER_SETUP_PHASE</a>



<a href="https://msdn.microsoft.com/a355dc8d-73f1-476b-a06f-24f011af4ace">CLUSTER_SETUP_PHASE_SEVERITY</a>



<a href="https://msdn.microsoft.com/515fe36d-84a0-41f1-80fa-a8c12718bdf5">CLUSTER_SETUP_PHASE_TYPE</a>



<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Cluster Management Functions</a>



<a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a>



<a href="https://msdn.microsoft.com/55e601de-b427-43cd-b7f8-6cc576077e59">DestroyCluster</a>



<a href="https://msdn.microsoft.com/f6ff92b7-608f-423c-9977-364a8eb44cec">MSCluster_EventClusterCallback</a>
 

 

