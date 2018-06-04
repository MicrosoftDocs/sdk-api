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

# _CLUSTER_SETUP_PHASE enumeration


## -description


Used by the 
    <a href="https://msdn.microsoft.com/fb7a6991-576c-4c03-aef0-89811fbc1a0d">ClusterSetupProgressCallback</a> function 
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




<a href="https://msdn.microsoft.com/fb7a6991-576c-4c03-aef0-89811fbc1a0d">ClusterSetupProgressCallback</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

