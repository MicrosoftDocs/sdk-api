---
UID: NC:clusapi.PCLUSTER_SETUP_PROGRESS_CALLBACK
title: PCLUSTER_SETUP_PROGRESS_CALLBACK (clusapi.h)
description: Callback function that receives regular updates on the progression of the setup of the cluster.
helpviewer_keywords: ["ClusterSetupPhaseAddClusterProperties","ClusterSetupPhaseAddNodeToCluster","ClusterSetupPhaseCleanupCOs","ClusterSetupPhaseCleanupNode","ClusterSetupPhaseClusterGroupOnline","ClusterSetupPhaseConfigureClusSvc","ClusterSetupPhaseConfigureClusterAccount","ClusterSetupPhaseContinue","ClusterSetupPhaseCoreGroupCleanup","ClusterSetupPhaseCreateClusterAccount","ClusterSetupPhaseCreateGroups","ClusterSetupPhaseCreateIPAddressResources","ClusterSetupPhaseCreateNetworkName","ClusterSetupPhaseCreateResourceTypes","ClusterSetupPhaseDeleteGroup","ClusterSetupPhaseEnd","ClusterSetupPhaseEvictNode","ClusterSetupPhaseFailureCleanup","ClusterSetupPhaseFatal","ClusterSetupPhaseFormingCluster","ClusterSetupPhaseGettingCurrentMembership","ClusterSetupPhaseInformational","ClusterSetupPhaseInitialize","ClusterSetupPhaseMoveGroup","ClusterSetupPhaseNodeUp","ClusterSetupPhaseOfflineGroup","ClusterSetupPhaseQueryClusterNameAccount","ClusterSetupPhaseStart","ClusterSetupPhaseStartingClusSvc","ClusterSetupPhaseValidateClusDisk","ClusterSetupPhaseValidateClusterNameAccount","ClusterSetupPhaseValidateNetft","ClusterSetupPhaseValidateNodeState","ClusterSetupPhaseWarning","ClusterSetupProgressCallback","ClusterSetupProgressCallback callback","ClusterSetupProgressCallback callback function [Failover Cluster]","PCLUSTER_SETUP_PROGRESS_CALLBACK","PCLUSTER_SETUP_PROGRESS_CALLBACK callback function [Failover Cluster]","clusapi/ClusterSetupProgressCallback","clusapi/PCLUSTER_SETUP_PROGRESS_CALLBACK","mscs.pcluster_setup_progress_callback"]
old-location: mscs\pcluster_setup_progress_callback.htm
tech.root: MsCS
ms.assetid: fb7a6991-576c-4c03-aef0-89811fbc1a0d
ms.date: 12/05/2018
ms.keywords: ClusterSetupPhaseAddClusterProperties, ClusterSetupPhaseAddNodeToCluster, ClusterSetupPhaseCleanupCOs, ClusterSetupPhaseCleanupNode, ClusterSetupPhaseClusterGroupOnline, ClusterSetupPhaseConfigureClusSvc, ClusterSetupPhaseConfigureClusterAccount, ClusterSetupPhaseContinue, ClusterSetupPhaseCoreGroupCleanup, ClusterSetupPhaseCreateClusterAccount, ClusterSetupPhaseCreateGroups, ClusterSetupPhaseCreateIPAddressResources, ClusterSetupPhaseCreateNetworkName, ClusterSetupPhaseCreateResourceTypes, ClusterSetupPhaseDeleteGroup, ClusterSetupPhaseEnd, ClusterSetupPhaseEvictNode, ClusterSetupPhaseFailureCleanup, ClusterSetupPhaseFatal, ClusterSetupPhaseFormingCluster, ClusterSetupPhaseGettingCurrentMembership, ClusterSetupPhaseInformational, ClusterSetupPhaseInitialize, ClusterSetupPhaseMoveGroup, ClusterSetupPhaseNodeUp, ClusterSetupPhaseOfflineGroup, ClusterSetupPhaseQueryClusterNameAccount, ClusterSetupPhaseStart, ClusterSetupPhaseStartingClusSvc, ClusterSetupPhaseValidateClusDisk, ClusterSetupPhaseValidateClusterNameAccount, ClusterSetupPhaseValidateNetft, ClusterSetupPhaseValidateNodeState, ClusterSetupPhaseWarning, ClusterSetupProgressCallback, ClusterSetupProgressCallback callback, ClusterSetupProgressCallback callback function [Failover Cluster], PCLUSTER_SETUP_PROGRESS_CALLBACK, PCLUSTER_SETUP_PROGRESS_CALLBACK callback function [Failover Cluster], clusapi/ClusterSetupProgressCallback, clusapi/PCLUSTER_SETUP_PROGRESS_CALLBACK, mscs.pcluster_setup_progress_callback
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PCLUSTER_SETUP_PROGRESS_CALLBACK
 - clusapi/PCLUSTER_SETUP_PROGRESS_CALLBACK
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - ClusterSetupProgressCallback callback
---

# PCLUSTER_SETUP_PROGRESS_CALLBACK callback function


## -description

Callback function that receives regular updates on the progression of the setup of the 
    cluster. This callback is used during processing of the 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-createcluster">CreateCluster</a>, 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-addclusternode">AddClusterNode</a>, and 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-destroycluster">DestroyCluster</a> functions.

## -parameters

### -param pvCallbackArg [in, optional]

<i>pvCallbackArg</i> parameter passed to the 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-createcluster">CreateCluster</a>, 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-addclusternode">AddClusterNode</a>, or 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-destroycluster">DestroyCluster</a> function.

### -param eSetupPhase [in]

Value from the <a href="/windows/desktop/api/clusapi/ne-clusapi-cluster_setup_phase">CLUSTER_SETUP_PHASE</a> enumeration 
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

Value from the <a href="/windows/desktop/api/clusapi/ne-clusapi-cluster_setup_phase_type">CLUSTER_SETUP_PHASE_TYPE</a> 
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
       <a href="/windows/desktop/api/clusapi/ne-clusapi-cluster_setup_phase_severity">CLUSTER_SETUP_PHASE_SEVERITY</a> enumeration 
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

### -param dwStatus [in] [in]

Status

## -returns

TBD

## -remarks

The <b>PCLUSTER_SETUP_PROGRESS_CALLBACK</b> type defines a pointer to this function.

The <a href="/previous-versions/windows/desktop/cluswmi/mscluster-eventclustercallback">MSCluster_EventClusterCallback</a> 
     MOF class is used in a similar manner.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-addclusternode">AddClusterNode</a>



<a href="/windows/desktop/api/clusapi/ne-clusapi-cluster_setup_phase">CLUSTER_SETUP_PHASE</a>



<a href="/windows/desktop/api/clusapi/ne-clusapi-cluster_setup_phase_severity">CLUSTER_SETUP_PHASE_SEVERITY</a>



<a href="/windows/desktop/api/clusapi/ne-clusapi-cluster_setup_phase_type">CLUSTER_SETUP_PHASE_TYPE</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-management-functions">Cluster Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-createcluster">CreateCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-destroycluster">DestroyCluster</a>



<a href="/previous-versions/windows/desktop/cluswmi/mscluster-eventclustercallback">MSCluster_EventClusterCallback</a>