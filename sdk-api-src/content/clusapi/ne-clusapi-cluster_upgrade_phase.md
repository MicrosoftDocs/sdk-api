---
UID: NE:clusapi._CLUSTER_UPGRADE_PHASE
title: CLUSTER_UPGRADE_PHASE (clusapi.h)
description: Describes the state of a rolling upgrade of the operating system on a cluster. This enumeration is used by the ClusterUpgradeProgressCallback callback function.
helpviewer_keywords: ["CLUSTER_UPGRADE_PHASE","CLUSTER_UPGRADE_PHASE enumeration [Failover Cluster]","ClusterUpgradePhaseInitialize","ClusterUpgradePhaseInstallingNewComponents","ClusterUpgradePhaseUpgradeComplete","ClusterUpgradePhaseUpgradingComponents","ClusterUpgradePhaseValidatingUpgrade","clusapi/CLUSTER_UPGRADE_PHASE","clusapi/ClusterUpgradePhaseInitialize","clusapi/ClusterUpgradePhaseInstallingNewComponents","clusapi/ClusterUpgradePhaseUpgradeComplete","clusapi/ClusterUpgradePhaseUpgradingComponents","clusapi/ClusterUpgradePhaseValidatingUpgrade","msclus/CLUSTER_UPGRADE_PHASE","msclus/ClusterUpgradePhaseInitialize","msclus/ClusterUpgradePhaseInstallingNewComponents","msclus/ClusterUpgradePhaseUpgradeComplete","msclus/ClusterUpgradePhaseUpgradingComponents","msclus/ClusterUpgradePhaseValidatingUpgrade","mscs.cluster_upgrade_phase"]
old-location: mscs\cluster_upgrade_phase.htm
tech.root: MsCS
ms.assetid: 75FB1BCD-03E0-4A6F-8C97-99AE8E958174
ms.date: 12/05/2018
ms.keywords: CLUSTER_UPGRADE_PHASE, CLUSTER_UPGRADE_PHASE enumeration [Failover Cluster], ClusterUpgradePhaseInitialize, ClusterUpgradePhaseInstallingNewComponents, ClusterUpgradePhaseUpgradeComplete, ClusterUpgradePhaseUpgradingComponents, ClusterUpgradePhaseValidatingUpgrade, clusapi/CLUSTER_UPGRADE_PHASE, clusapi/ClusterUpgradePhaseInitialize, clusapi/ClusterUpgradePhaseInstallingNewComponents, clusapi/ClusterUpgradePhaseUpgradeComplete, clusapi/ClusterUpgradePhaseUpgradingComponents, clusapi/ClusterUpgradePhaseValidatingUpgrade, msclus/CLUSTER_UPGRADE_PHASE, msclus/ClusterUpgradePhaseInitialize, msclus/ClusterUpgradePhaseInstallingNewComponents, msclus/ClusterUpgradePhaseUpgradeComplete, msclus/ClusterUpgradePhaseUpgradingComponents, msclus/ClusterUpgradePhaseValidatingUpgrade, mscs.cluster_upgrade_phase
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
req.typenames: CLUSTER_UPGRADE_PHASE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSTER_UPGRADE_PHASE
 - clusapi/_CLUSTER_UPGRADE_PHASE
 - CLUSTER_UPGRADE_PHASE
 - clusapi/CLUSTER_UPGRADE_PHASE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUSTER_UPGRADE_PHASE
---

# CLUSTER_UPGRADE_PHASE enumeration


## -description

Describes the state of a rolling upgrade of the operating system on a cluster. This enumeration is used by the <a href="/windows/desktop/api/clusapi/nc-clusapi-pcluster_upgrade_progress_callback">ClusterUpgradeProgressCallback</a> callback function.

## -enum-fields

### -field ClusterUpgradePhaseInitialize:1

The nodes are being notified that an upgrade has started.

### -field ClusterUpgradePhaseValidatingUpgrade:2

The updated is being validated to determine whether the all of nodes in the cluster can be upgraded.

### -field ClusterUpgradePhaseUpgradingComponents:3

The nodes are being upgraded.

### -field ClusterUpgradePhaseInstallingNewComponents:4

The new resources are being installed.

### -field ClusterUpgradePhaseUpgradeComplete:5

The upgrade is complete.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterupgradefunctionallevel">ClusterUpgradeFunctionalLevel</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
