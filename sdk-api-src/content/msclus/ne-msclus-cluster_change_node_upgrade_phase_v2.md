---
UID: NE:msclus.CLUSTER_CHANGE_NODE_UPGRADE_PHASE_V2
title: CLUSTER_CHANGE_NODE_UPGRADE_PHASE_V2
author: windows-sdk-content
description: Defines the notifications that are generated for the upgrade of a cluster node.
old-location: mscs\cluster_change_node_upgrade_phase_v2.htm
tech.root: mscs
ms.assetid: 70EEDB16-CEE0-4570-9DBD-1649DD800453
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CLUSTER_CHANGE_NODE_UPGRADE_PHASE_V2, CLUSTER_CHANGE_NODE_UPGRADE_PHASE_V2 enumeration [Failover Cluster], CLUSTER_CHANGE_UPGRADE_ALL, CLUSTER_CHANGE_UPGRADE_NODE_COMMIT, CLUSTER_CHANGE_UPGRADE_NODE_POSTCOMMIT, CLUSTER_CHANGE_UPGRADE_NODE_PREPARE, clusapi/CLUSTER_CHANGE_NODE_UPGRADE_PHASE_V2, clusapi/CLUSTER_CHANGE_UPGRADE_ALL, clusapi/CLUSTER_CHANGE_UPGRADE_NODE_COMMIT, clusapi/CLUSTER_CHANGE_UPGRADE_NODE_POSTCOMMIT, clusapi/CLUSTER_CHANGE_UPGRADE_NODE_PREPARE, msclus/CLUSTER_CHANGE_NODE_UPGRADE_PHASE_V2, msclus/CLUSTER_CHANGE_UPGRADE_ALL, msclus/CLUSTER_CHANGE_UPGRADE_NODE_COMMIT, msclus/CLUSTER_CHANGE_UPGRADE_NODE_POSTCOMMIT, msclus/CLUSTER_CHANGE_UPGRADE_NODE_PREPARE, mscs.cluster_change_node_upgrade_phase_v2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: msclus.h
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
 - CLUSTER_CHANGE_NODE_UPGRADE_PHASE_V2
product: Windows
targetos: Windows
req.typenames: CLUSTER_CHANGE_NODE_UPGRADE_PHASE_V2
req.redist: 
---

# CLUSTER_CHANGE_NODE_UPGRADE_PHASE_V2 enumeration


## -description


Defines the notifications that are generated for the upgrade of a cluster node.


## -enum-fields




### -field CLUSTER_CHANGE_UPGRADE_NODE_PREPARE

Indicates that the upgrade is being prepared.


### -field CLUSTER_CHANGE_UPGRADE_NODE_COMMIT

Indicates that the upgrade is in progress.


### -field CLUSTER_CHANGE_UPGRADE_NODE_POSTCOMMIT

Indicates that the upgrade is finished.


### -field CLUSTER_CHANGE_UPGRADE_ALL

Indicates all <b>CLUSTER_CHANGE_NODE_UPGRADE_PHASE_V2</b> notifications.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

