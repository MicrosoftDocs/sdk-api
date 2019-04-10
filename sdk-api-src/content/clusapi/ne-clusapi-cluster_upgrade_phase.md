---
UID: NE:clusapi._CLUSTER_UPGRADE_PHASE
title: CLUSTER_UPGRADE_PHASE (clusapi.h)
author: windows-sdk-content
description: Describes the state of a rolling upgrade of the operating system on a cluster. This enumeration is used by the ClusterUpgradeProgressCallback callback function.
old-location: mscs\cluster_upgrade_phase.htm
tech.root: MsCS
ms.assetid: 75FB1BCD-03E0-4A6F-8C97-99AE8E958174
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CLUSTER_UPGRADE_PHASE, CLUSTER_UPGRADE_PHASE enumeration [Failover Cluster], ClusterUpgradePhaseInitialize, ClusterUpgradePhaseInstallingNewComponents, ClusterUpgradePhaseUpgradeComplete, ClusterUpgradePhaseUpgradingComponents, ClusterUpgradePhaseValidatingUpgrade, clusapi/CLUSTER_UPGRADE_PHASE, clusapi/ClusterUpgradePhaseInitialize, clusapi/ClusterUpgradePhaseInstallingNewComponents, clusapi/ClusterUpgradePhaseUpgradeComplete, clusapi/ClusterUpgradePhaseUpgradingComponents, clusapi/ClusterUpgradePhaseValidatingUpgrade, msclus/CLUSTER_UPGRADE_PHASE, msclus/ClusterUpgradePhaseInitialize, msclus/ClusterUpgradePhaseInstallingNewComponents, msclus/ClusterUpgradePhaseUpgradeComplete, msclus/ClusterUpgradePhaseUpgradingComponents, msclus/ClusterUpgradePhaseValidatingUpgrade, mscs.cluster_upgrade_phase
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: CLUSTER_UPGRADE_PHASE
req.redist: 
---

# CLUSTER_UPGRADE_PHASE enumeration


## -description


Describes the state of a rolling upgrade of the operating system on a cluster. This enumeration is used by the <a href="https://msdn.microsoft.com/EE803D8C-3EFD-414F-8E38-65A1DFA8079B">ClusterUpgradeProgressCallback</a> callback function.


## -enum-fields




### -field ClusterUpgradePhaseInitialize

The nodes are being notified that an upgrade has started.


### -field ClusterUpgradePhaseValidatingUpgrade

The updated is being validated to determine whether the all of nodes in the cluster can be upgraded.


### -field ClusterUpgradePhaseUpgradingComponents

The nodes are being upgraded.


### -field ClusterUpgradePhaseInstallingNewComponents

The new resources are being installed.


### -field ClusterUpgradePhaseUpgradeComplete

The upgrade is complete.


## -see-also




<a href="https://msdn.microsoft.com/EA013501-A4E2-48D8-9062-D20141485CC5">ClusterUpgradeFunctionalLevel</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

