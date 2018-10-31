---
UID: NE:clusapi._CLUSTER_SETUP_PHASE
title: "_CLUSTER_SETUP_PHASE"
author: windows-sdk-content
description: Used by the ClusterSetupProgressCallback function to identify the current phase of the cluster setup process.
old-location: mscs\cluster_setup_phase.htm
tech.root: mscs
ms.assetid: cc881b92-c312-4b88-8d8d-09f98925b5b5
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CLUSTER_SETUP_PHASE, CLUSTER_SETUP_PHASE enumeration [Failover Cluster], ClusterSetupPhaseAddClusterProperties, ClusterSetupPhaseAddNodeToCluster, ClusterSetupPhaseCleanupCOs, ClusterSetupPhaseCleanupNode, ClusterSetupPhaseClusterGroupOnline, ClusterSetupPhaseConfigureClusSvc, ClusterSetupPhaseConfigureClusterAccount, ClusterSetupPhaseCoreGroupCleanup, ClusterSetupPhaseCreateClusterAccount, ClusterSetupPhaseCreateGroups, ClusterSetupPhaseCreateIPAddressResources, ClusterSetupPhaseCreateNetworkName, ClusterSetupPhaseCreateResourceTypes, ClusterSetupPhaseDeleteGroup, ClusterSetupPhaseEvictNode, ClusterSetupPhaseFailureCleanup, ClusterSetupPhaseFormingCluster, ClusterSetupPhaseGettingCurrentMembership, ClusterSetupPhaseInitialize, ClusterSetupPhaseMoveGroup, ClusterSetupPhaseNodeUp, ClusterSetupPhaseOfflineGroup, ClusterSetupPhaseQueryClusterNameAccount, ClusterSetupPhaseStartingClusSvc, ClusterSetupPhaseValidateClusDisk, ClusterSetupPhaseValidateClusterNameAccount, ClusterSetupPhaseValidateNetft, ClusterSetupPhaseValidateNodeState, _CLUSTER_SETUP_PHASE, clusapi/CLUSTER_SETUP_PHASE, clusapi/ClusterSetupPhaseAddClusterProperties, clusapi/ClusterSetupPhaseAddNodeToCluster, clusapi/ClusterSetupPhaseCleanupCOs, clusapi/ClusterSetupPhaseCleanupNode, clusapi/ClusterSetupPhaseClusterGroupOnline, clusapi/ClusterSetupPhaseConfigureClusSvc, clusapi/ClusterSetupPhaseConfigureClusterAccount, clusapi/ClusterSetupPhaseCoreGroupCleanup, clusapi/ClusterSetupPhaseCreateClusterAccount, clusapi/ClusterSetupPhaseCreateGroups, clusapi/ClusterSetupPhaseCreateIPAddressResources, clusapi/ClusterSetupPhaseCreateNetworkName, clusapi/ClusterSetupPhaseCreateResourceTypes, clusapi/ClusterSetupPhaseDeleteGroup, clusapi/ClusterSetupPhaseEvictNode, clusapi/ClusterSetupPhaseFailureCleanup, clusapi/ClusterSetupPhaseFormingCluster, clusapi/ClusterSetupPhaseGettingCurrentMembership, clusapi/ClusterSetupPhaseInitialize, clusapi/ClusterSetupPhaseMoveGroup, clusapi/ClusterSetupPhaseNodeUp, clusapi/ClusterSetupPhaseOfflineGroup, clusapi/ClusterSetupPhaseQueryClusterNameAccount, clusapi/ClusterSetupPhaseStartingClusSvc, clusapi/ClusterSetupPhaseValidateClusDisk, clusapi/ClusterSetupPhaseValidateClusterNameAccount, clusapi/ClusterSetupPhaseValidateNetft, clusapi/ClusterSetupPhaseValidateNodeState, mscs.cluster_setup_phase
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
 - CLUSTER_SETUP_PHASE
product: Windows
targetos: Windows
req.typenames: CLUSTER_SETUP_PHASE
req.redist: 
---

# _CLUSTER_SETUP_PHASE enumeration


## -description


Used by the 
    <a href="https://msdn.microsoft.com/en-us/library/Bb394687(v=VS.85).aspx">ClusterSetupProgressCallback</a> function 
    to identify the current phase of the cluster setup process.


## -enum-fields




### -field ClusterSetupPhaseInitialize

Initialize cluster setup.


### -field ClusterSetupPhaseValidateNodeState

Validate cluster nodes.


### -field ClusterSetupPhaseValidateNetft

Validate cluster networks.


### -field ClusterSetupPhaseValidateClusDisk

Validate cluster disks.


### -field ClusterSetupPhaseConfigureClusSvc

Configure cluster service.


### -field ClusterSetupPhaseStartingClusSvc

Start  cluster service.


### -field ClusterSetupPhaseQueryClusterNameAccount

Query cluster name.


### -field ClusterSetupPhaseValidateClusterNameAccount

Validate cluster name.


### -field ClusterSetupPhaseCreateClusterAccount

Create cluster account.


### -field ClusterSetupPhaseConfigureClusterAccount

Configure cluster account.


### -field ClusterSetupPhaseFormingCluster

Form the cluster.


### -field ClusterSetupPhaseAddClusterProperties

Add properties to cluster.


### -field ClusterSetupPhaseCreateResourceTypes

Create resource types.


### -field ClusterSetupPhaseCreateGroups

Create resource groups.


### -field ClusterSetupPhaseCreateIPAddressResources

Create IP address resources.


### -field ClusterSetupPhaseCreateNetworkName

Create network name.


### -field ClusterSetupPhaseClusterGroupOnline

Bring cluster groups online.


### -field ClusterSetupPhaseGettingCurrentMembership

Get current cluster membership.


### -field ClusterSetupPhaseAddNodeToCluster

Add node to cluster membership.


### -field ClusterSetupPhaseNodeUp

Start node.


### -field ClusterSetupPhaseMoveGroup

Move group to another node.


### -field ClusterSetupPhaseDeleteGroup

Delete group from cluster.


### -field ClusterSetupPhaseCleanupCOs

Clean up offline group.


### -field ClusterSetupPhaseOfflineGroup

Move group offline.


### -field ClusterSetupPhaseEvictNode

Remove a node from the cluster.


### -field ClusterSetupPhaseCleanupNode

Return node to pre-clustered state.


### -field ClusterSetupPhaseCoreGroupCleanup

Return core resource group to pre-clustered state.


### -field ClusterSetupPhaseFailureCleanup

Return failed resource to pre-clustered state.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb394687(v=VS.85).aspx">ClusterSetupProgressCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb309147(v=VS.85).aspx">Failover Cluster Enumerations</a>
 

 

